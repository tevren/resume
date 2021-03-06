# The Rakefile does all of the real work.

require 'rubygems'
require 'bundler'
Bundler.require(:default)

task :default => [:github]

desc "Run your resume locally."
task :local do
  Kernel.exec("shotgun -d -s thin -p 9393")
end

# TODO: Make this dynamically figure out all of the files needed from Sinatra.
desc "Deploy to remote defined in config.yaml"
task :github do
  require File.expand_path('../resume',__FILE__)

  remote = YAML.load_file('config.yaml')['github']['remote']

  browser = Rack::Test::Session.new(Rack::MockSession.new(Sinatra::Application))

  files = [
    'index.html',
    'resume.txt',
    'resume.pdf',
    'avatar.png'
  ]

  files += Dir.entries("public").keep_if {|file| File.file? "public/#{file}"}
  files += Dir.entries("public/css").keep_if {|file| File.file? "public/css/#{file}"}.map {|f| "css/#{f}" }

  p files

  root = "/tmp/checkout-#{Time.now.to_i}"
  g = Git.clone(remote.insert(8,"#{ENV['GH_TOKEN']}@"), root, :log => Logger.new(STDOUT))
  g.config('user.name', 'Anurag Mohanty')
  g.config('user.email', '805123+tevren@users.noreply.github.com')
  # Make sure this actually switches branches.
  g.checkout(g.branch('gh-pages'))

  Dir.entries(root).keep_if {|f| File.file? f}.each {|f| g.remove f }

  files.each {|file|
    browser.get file
    content = browser.last_response.body
    FileUtils.mkdir_p("#{root}/#{File.dirname(file)}")
    File.open("#{root}/#{file}", 'w') {|f| f.write(content) }
    puts "#{file} => #{root}/#{file}"
    g.add(file)
  }

  g.commit('Regenerating Github Pages.')

  # PUSH!
  g.push(g.remote('origin'), g.branch('gh-pages'))

  puts '--> GitHub Pages Commit and Push successful.'
end

desc "Generate a PDF of your resume."
task :pdf do
  require File.expand_path('../resume',__FILE__)
  remote = YAML.load_file('config.yaml')['github']['remote']
  browser = Rack::Test::Session.new(Rack::MockSession.new(Sinatra::Application))
  html_file = browser.get('/index.html').body
  root_dir = File.dirname(__FILE__)
  kit = PDFKit.new(html_file, :page_size => 'Letter', :enable_local_file_access => true)
  kit.stylesheets << "#{root_dir}/public/css/markdown.css"
  kit.to_file("#{root_dir}/resume.pdf")
  puts '--> Successfully generated PDF.'
end

task :github => :pdf