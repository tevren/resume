#Anurag Mohanty
##Systems Engineer

> [github/tevren](http://github.com/tevren)</br>
> [anurag@mohanty.io](mailto:anurag@mohanty.io)</br>
> [(516) 218-1593](tel:+15162181593)</br>

-----
### Technical

|||||
|---|---|---|---|
| AWS| Ruby | Ruby on Rails | Graphite
| Chef| Bash|Sinatra | Nagios|
| Puppet | Perl|Play Framework | New Relic
| MySQL | Mcollective| Dropwizard | ELK
| MongoDB | RabbitMQ | Kickstart
| Jenkins | Squid
| Artifactory |

-----

### Experience

#### Amplify Education _December 2012 to Present_
##### Systems Engineer
- Built deployment pipeline for Java and JRuby web-applications.
  - Wrote guidelines and documentation on application configuration and monitoring.
  - Designed criteria for build-manifests, which describe set of applications have been tested together and can be released through the deployment pipeline together. 
  - Extended Mcollective as a deployment mechanism by using RabbitMQ, resulting in dependable and scalable push button deployments.
  - Maintained Jenkins server and agents.
  - Built Artifactory architecture which included S3 storage back-end, and MySQL on Amazon RDS, and cross-region Artifactory replication for disaster recovery.
- Responsibilities include maintaining and monitoring hundreds of servers on AWS that communicated with 20,000 tablets.
- Designed the AWS architecture, including VPC/subnet layouts.
- Designed git-based Chef workflow/architecture orchestrated by Jenkins.
  - Implemented role cookbooks to improve cookbook versioning and dependency management across a growing organization.
  - Authored Knife plug-in to automate node removal from EC2 and Chef. The plug in schedules downtime in Nagios, removes the client from chef, terminates the EC2 instance and cleans up any leftover AWS resources such as Route53 records, EBS volumes AND Elastic IPs.
  - Collaborated with developers to write Chef cookbooks to ensure applications were properly configured.
  - Worked with developers to ensure their applications met production readiness requirements in terms of monitoring and configuration.
- Administered Nagios and wrote Nagios checks as part of application on-boarding and on-going application monitoring.
- Built and deployed RabbitMQ infrastructure.
  - Wrote ruby scripts that test end to end availability of RabbitMQ cluster and sent usage data to Graphite.
  - Provided support and expertise to development team in dealing with RabbitMQ.
- Administered ElasticSearch cluster which served as back-end to our logging infrastructure.
- Responsible for in-house appliance from the imaging process at vendor factories to deployment + maintenance at customers' facilities.
- Built HTTP content filtering farm on AWS using Dansguardian and Squid.
- Member of daily on-call rotation that is responsible for resolving outages reported by customers to Tier 3 and of a weekly on-call rotation that is responsible for uptime of critical services.
- Automated migration from Exchange to Google Apps using a combination of GAM and custom scripting.

**Technical Environment:** AWS, Chef, Java, Play, JRuby, MySQL, Git, Stash, Jenkins, Artifactory, Graphite, Nagios, ELK, Kickstart.

#### Columbia University Libraries _January 2010 to December 2012_
##### Systems Engineer
- Managed all Apple Macintosh environments through Columbia University Libraries.
  - Built Imaging + Deployment pipeline for OSX machines using Deploy Studio.
  - Tested and deployed Munki as a solution to manage and update software across environments.
- Wrote Ruby on Rails applications as front-ends to various back-end systems.
  - Created a front-end for Munki so that support engineers can manage software through a web portal.
  - Developed an Ruby on Rails application to create help desk tickets. 
- Documented procedures and best practices for various technical tasks performed by the technology team.
- Wrote Perl scripts to generate reports for librarians.
- Maintained JIRA instance used to track help-desk tickets across Columbia University Libraries.

**Technical Environment:** Ruby, Ruby on Rails, Perl, JIRA, Oracle Database, Bash, OSX, Munki, Deploy Studio.

#### Columbia University Medical Center _June 2007 to December 2009_
##### Systems Administrator and Programmer
- Authored various patient file management scripts.</br>
- Automated file server backups and data archival. </br>
- Developed VB.NET programs to interface with scanner.</br>
- Wrote programs in VB.Net to automate the process of transitioning from paper records to digital records.

**Technical Environment:** VBScript, VB.Net, Winbatch.</br>

-----

### Projects

1. **Biffbot**</br>
  [Biffbot](https://github.com/tevren/biffbot)
  is a ruby library for the [Diffbot](https://www.diffbot.com) API.

2. **RubySpark**</br>
  [RubySpark](https://github.com/tevren/rubyspark)
  is a ruby port of <a href=http://zachholman.com/spark/>spark</a>.

-----

### Education

#### Bachelor of Science in Applied Mathematics _2004 to 2009_ </br>
  University of Massachusetts at Amherst, Massachusetts
