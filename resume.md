# Anurag Mohanty

## Site Reliability Engineer

> [github/tevren](http://github.com/tevren)</br>
> [anurag@mohanty.io](mailto:anurag@mohanty.io)</br>
> [(516) 218-1593](tel:+15162181593)</br>

-----
### Technical Skills
||||||
|---|---|---|---|---|
| GCP| Python| Docker | Terraform | Datadog
| AWS | Golang | Kubernetes | Pulumi | NewRelic
| Azure | Ruby | Helm | Chef | CircleCI
| Digital Ocean  | Shell | Mesos/Marathon | Ansible |Jenkins

-----

### Experience

#### FuboTV _August 2017 to Present_
##### Staff Site Reliability Engineer _August 2019 to Present_
- Migrated applications from in house python deployment tool to Helm.
- Took initiative to discover root cause of an ever-growing Datadog bill, and worked with engineering teams to implement a solution saving the company $97,000 annually.
- Designed and implemented HA Apache Kafka + Zookeeper infrastructure.
- Developed disaster recovery in the video playout stack that allows for the loss of an entire GCP region. This architecture is extendable across cloud providers. 
- Ensured the video engineering team's data handling met GDPR requirements.
- Authored golang application that manages video metadata. It served as a guideline on how services are written on the video engineering team.
- Authored libraries used in the video ingest and playout stack to interface with in-house application fronting Apache Kafka.
- Wrote golang service that aggregates data from BigQuery and sends resultant data to Datadog. This service filled a gap in our monitoring by providing latency metrics that were otherwise unavailable.
- Identified and fixed concurrency bugs in multiple critical systems. These range from improving write performance in the metadata library by tracing slow database queries and implementing concurrency to solving race conditions with multiple locks. 

##### Senior Site Reliability Engineer _August 2017 to August 2019_
- Original author and primary maintainer of a Python-based deployment orchestration that creates and manages Kubernetes deployments across multiple environments and clusters.
- Designed and wrote a Golang service that reduces writes to Google Cloud Storage, which resulted in the company saving $40,000 a month.
- Helped scale a Redis-backed service that supports over 200,000 concurrent users, a tenfold increase over the previous year.
- Added monitoring and alerting to key services.
- Developed a zero user impact rollout and update strategy for storage backends (redis, kafka).
- Relied upon by leadership and multiple teams for SRE expertise.

**Technical Environment:** Google Cloud, Kubernetes, Golang, Python 2.7/3, CircleCI, Redis, Postgres, Kafka, Datadog, CircleCI

#### Spotify  _June 2016 to July 2017_
##### Senior Site Reliability Engineer
- Worked on internal application that provided a uniform experience between GCP compute provisioning and on premise hardware provisioning.
  - Wrote Python app that consumes pubsub messages and restarts machines.
  - Improved provisioning for physical machines by adding automated testing.
  - Migrated Python web application stack to Docker for ease of local development.
- Drafted design documentation for large infrastructure changes, including reducing deltas in deployments to speed up DNS deployments.
- Member of weekly on-call rotation that is responsible for uptime of critical services developed by the team, including DNS and Google Cloud infrastructure.

**Technical Environment:** Google Cloud, Python 2.7/3, Puppet, Jenkins, Redis, Zookeeper, Helios.

#### Amplify Education _December 2012 to June 2016_
##### Systems Engineer
- Built deployment pipeline for Java and JRuby web-applications.
  - Wrote guidelines and documentation on application configuration and monitoring.
  - Designed criteria for build-manifests, which describe sets of applications that have been tested together and can be released through the deployment pipeline together.
  - Extended Mcollective as a deployment mechanism by using RabbitMQ, resulting in dependable and scalable push button deployments.
  - Maintained Jenkins server and agents.
  - Built Artifactory architecture which included S3 storage back-end, MySQL on Amazon RDS, and cross-region Artifactory replication for disaster recovery.
- Responsibilities include maintaining and monitoring hundreds of servers on AWS that communicated with 20,000 tablets.
- Designed the AWS architecture, including VPC/subnet layouts.
- Designed git-based Chef workflow/architecture orchestrated by Jenkins.
  - Implemented role cookbooks to improve cookbook versioning and dependency management across a growing organization.
  - Authored Knife plug-in to automate host termination including cleanup of Chef, Nagios, EC2 instances, Route 53 records, EBS volumes, and Elastic IPs.
  - Collaborated with developers to write Chef cookbooks to ensure applications were properly configured.
- Held production readiness reviews with developers to ensure applications met monitoring and configuration requirements.
- Administered Nagios and wrote Nagios checks as part of application on-boarding and on-going application monitoring.
- Built and deployed RabbitMQ infrastructure.
  - Wrote ruby scripts that test end to end availability of RabbitMQ cluster and sent usage data to Graphite.
  - Provided support and expertise to development team in dealing with RabbitMQ.
- Administered ElasticSearch cluster which served as back-end to our logging infrastructure.
- Developed imaging workflow for customer hosted appliance for unattended provisioning at vendor's factories.
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
- Authored various patient file management scripts.
- Automated file server backups and data archival.
- Developed VB.NET programs to interface with scanner.
- Wrote programs in VB.Net to automate the process of transitioning from paper records to digital records.

**Technical Environment:** VBScript, VB.Net, Winbatch.</br>

-----

### Projects

1. **Biffbot**</br>
  [Biffbot](https://github.com/tevren/biffbot)
  is a ruby library for the [Diffbot](https://www.diffbot.com) API.

2. **RubySpark**</br>
  [RubySpark](https://github.com/tevren/rubyspark)
  is a ruby port of [spark](http://zachholman.com/spark/).

-----

### Education

#### Bachelor of Science in Applied Mathematics _2004 to 2009_ </br>
  University of Massachusetts at Amherst, Massachusetts
