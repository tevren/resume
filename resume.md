# Anurag Mohanty
## Systems Engineer

> [github/tevren](http://github.com/tevren)</br>
> [anurag@mohanty.io](mailto:anurag@mohanty.io)</br>
> [(516) 218-1593](tel:+15162181593)</br>

-----
### Technical
1. AWS
2. Amazon Web Stack
3. Chef
4. Puppet 
5. Ruby
6. Perl
7. Git
8. MySQL
9. MongoDB
10. RDS
11. Graphite
12. Nagios
13. ELK
14. Play
15. Ruby on Rails
16. Sinatra
18. Dropwizard
19. Jenkins
20. Artifactory
21. Squid
22. Kickstart
23. Mcollective
24. RabbitMQ

-----
### Experience

**Amplify Education** _December 2012 to Present_</br>
*Systems Engineer*</br>
Responsibilities include maintaining and monitoring hundreds of servers on AWS that communicated with 20,000 tablets.</br>
Maintained Jenkins server and agents, as well as the build pipeline.
Wrote guidelines and documentation on application configuration and monitoring.</br>
Designed the AWS architecture, including VPC/subnet layouts.</br>
Designed Chef workflow and architecture, for the Access division, and for the entire company as well. The workflow is git-based with Jenkins testing and deploying changes to the chef server.</br>
Solved the problem dependency resolution and conflicting cookbook versions by implementing role based cookbooks and moving dependencies from environment files to role cookbooks.</br> 
Authored Knife plugin to automate node from EC2 and Chef. The plugin schedules downtime in nagios, removes the client from chef, terminates the EC2 instance and cleans up any leftover AWS resources such as Route53 records, EBS volumes AND Elastic IPs.</br>
Designed criteria for build manifests, essential requirements for applications to be pushed through the build pipeline.</br>
Designed build pipeline for java and ruby web-applications. This included designing how applications would be built and tested, and deployment of the built artifacts through the pipeline into production.</br>
Worked with developers to on board their applications into the build pipeline. On boarding includes ensuring that ensure dependencies were met, that monitoring criteria, and application configuration guidelines were met.</br>
Built artifactory architecture which included S3 back-end for storage, and MySQL on RDS as a database, and cross-region Artifactory replication.</br>
Administered nagios and wrote nagios checks as part of application on-boarding and on-going application monitoring.</br>
Built RabbitMQ cluster and wrote end to end monitoring scripts to ensure the cluster healthy and able to route messages.</br>
Wrote ruby script to monitor RabbitMQ usage and send usage data to Graphite.</br>
Administered ElasticSearch cluster which served as back-end to our logging infrastructure.</br>
Extended mcollective as a deployment mechanism by using RabbitMQ, resulting in dependable and scalable push button deployments across our AWS environments.</br>
Responsible for in-house CDNs from the imaging process at vendor factories to deployment + maintenance at customers' facilities.</br>
Designed and built content filtering farm on AWS. At its peak 20,000 tablets connected to the farm via VPN and had their traffic routed by Squid to HTTPS and HTTP filtering applications.</br>
Collaborated with developers to write Chef cookbooks to ensure applications were properly configured.</br>
Member of daily on-call rotation that is responsible for resolving outages reported by customers to Tier 3 and of a weekly on-call rotation that is responsible for uptime of critical services.</br>
**Technical Environment:** AWS, Chef, Java, Play, Ruby, MySQL, Git, Stash, Jenkins, Artifactory, Graphite, Nagios, ELK, Kickstart
  
**Columbia University Libraries** _January 2010 to December 2012_</br>
*Systems Engineer*</br> 
Managed all Apple Macintosh environments through Columbia University Libraries.</br>
Wrote Ruby on Rails applications as front-ends to various back-end systems.</br> 
Documented procedures and best practices for various technical tasks performed by the technology team.</br>
Wrote Perl scripts to generate reports for librarians.</br> 
Maintained JIRA instance used to track help-desk tickets across Columbia University Libraries.</br>
**Technical Environment:** Ruby, Ruby on Rails, Perl, JIRA, Oracle Database, Bash, OSX, Munki, Deploy Studio

**Columbia University Medical Center** _June 2007 to December 2009_</br>
*Systems Administrator and Programmer*</br> 
Authored various patient file management scripts.</br> 
Automated file server backups and data archival. </br>
Developed VB.NET programs to interface with scanner.</br>
Wrote programs in VB.Net to automate the process of transitioning from paper records to digital records.</br>
**Technical Environment:** VBScript, VB.Net, Winbatch, Windows XP
    
-----
### Projects

* **Biffbot**</br>
  <a href=https://github.com/tevren/biffbot>Biffbot</a>
  is a ruby libary for the <a href=https://www.diffbot.com >Diffbot</a> API.

* **RubySpark**</br>
  <a href=https://github.com/tevren/rubyspark>RubySpark</a>
  is a ruby port of <a href=http://zachholman.com/spark/>spark</a>.

-----
### Education

**Bachelor of Science in Applied Mathematics** _2004 to 2009_ </br>
  University of Massachusetts at Amherst, Massachusetts

