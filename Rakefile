# The Rakefile does all of the real work.

require 'rubygems'
require 'bundler'
Bundler.require(:default)

task :default => [:github]

desc "Run your resume locally."
task :local do
  Kernel.exec("shotgun -d -s thin -p 9393")
end

# Based off of http://railspikes.com/2010/2/13/rake-task-for-deploying-to-heroku
desc "Deploy to Heroku."
task :heroku do
  [ 'heroku', 'heroku/command', 'git' ].each {|gem|
    begin
      require gem
    rescue LoadError
      puts "The gem #{gem} is not installed.\n"
      exit
    end
  }

  puts 'Deploying to Heroku. If you haven\'t run heroku create before, this will fail.'

  # Get users credentials
  user, pass = File.read(File.expand_path("~/.heroku/credentials")).split("\n")
  heroku = Heroku::Client.new(user, pass)

  cmd = Heroku::Command::BaseWithApp.new([])
  remotes = cmd.git_remotes '.'
  remote, app = remotes.detect {|key, value| value == (ENV['APP'] || cmd.app)}

  if remote.nil?
    raise "Could not find a git remote for the '#{ENV['APP']}' app"
  end

  g = Git.open('.')
  g.push(g.remote(remote))

  heroku.rake(app, "db:migrate")
  heroku.restart(app)

  puts '--> Heroku Push successful.'
end

# TODO: Make this dynamically figure out all of the files needed from Sinatra.
desc "Deploy to remote defined in config.yaml"
task :github do
  require File.expand_path('../resume',__FILE__)

  remote = YAML.load_file('config.yaml')['github']['remote']

  browser = Rack::Test::Session.new(Rack::MockSession.new(Sinatra::Application))

  files = [
    'index.html',
    'resume.txt'
  ]

  files += Dir.entries("public").keep_if {|file| File.file? "public/#{file}"}
  files += Dir.entries("public/css").keep_if {|file| File.file? "public/css/#{file}"}.map {|f| "css/#{f}" }

  p files

  root = "/tmp/checkout-#{Time.now.to_i}"
  g = Git.clone(remote, root, :log => Logger.new(STDOUT))

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
