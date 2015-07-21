#Jenkins
Jenkins is an open source continuous integration tool written in Java.

Continuous Integration, in its simplest form, involves a tool that monitors your version control system
for changes. Whenever a change is detected, this tool automatically compiles and tests your application.
If something goes wrong, the tool immediately notifies the developers so that they can fix the issue
immediately.

![jenkins workflow](https://cloud.githubusercontent.com/assets/3624858/8793796/38867792-2f99-11e5-89cf-a2361df0b102.png)

Continuous Integration is about reducing risk by providing faster feedback

##Jenkins Tool

#### Code Repositories
 SVN, Mercurial, Git
 
####Continuous Build Systems
 Jenkins, Bamboo, Cruise Control

#### Test Frameworks
 JUnit,Cucumber, CppUnit

#### Artifact Repositories
 Nexus, Artifactory, Archiva

##What can Jenkins do?

 Generate test reports
 Integrate with many different Version Control Systems
 Push to various artifact repositories
 Deploys directly to production or test environments
 Notify stakeholders of build status
 …and much more  
 
 ##How Jenkins works 
 
#### Setup
 
 * When setting up a project in Jenkins, out of the box you have options
 * Associating with a version control server
 * Triggering builds
 * Polling, Periodic, Building based on other projects
 * Execution of shell scripts, bash scripts, Ant targets, and Maven
 targets
 * Artifact archival
 * Publish JUnit test results and Javadocs
 * Email notifications
 * As stated earlier, plugins expand the functionality even
further 

##How Jenkins works - Building

 * Once a project is successfully created in Jenkins, all future
builds are automatic
 Building
 * Jenkins executes the build in an executer
 * By default, Jenkins gives one executer per core on the build server
 * Jenkins also has the concept of slave build servers
 * Useful for building on different architectures
 * Distribution of load 

##How Jenkins works - Reporting

 * Jenkins comes with basic reporting features
 * Keeping track of build status
 * Last success and failure
 * “Weather” – Build trend
 * These can be greatly enhanced with the use of pre-build
plugins
 * Unit test coverage
 * Test result trending
 * Findbugs, Checkstyle, PMD 
designed to help identify and fix integration and regression issues faster, resulting in
smoother, quicker delivery, and fewer bugs

Continuous Integration helps you
get your software into the hands of the testers and the end users faster, more reliably, and with less effort.

The practice of automatically deploying every successful build directly into production is
generally known as Continuous Deployment.

http://www.bogotobogo.com/DevOps/Jenkins/images/Intro_install/jenkins-the-definitive-guide.pdf
http://www.cs.colorado.edu/~kena/classes/5828/s12/presentation-materials/bowesjesse.pdf
