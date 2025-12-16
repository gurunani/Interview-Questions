
### 1. What are the popular DevOps tools that you use?
**A:**

```bash
We use following tools for work in DevOps:
 * Jenkins: Jenkins is an open-source automation server used for building, testing, and deploying code. We use Jenkins to create and manage CI/CD pipelines, automating the software delivery process.
 * Terraform: Terraform is an IaC (Infrastructure as Code) tool that allows for the provisioning and management of infrastructure resources. We use Terraform to define and deploy infrastructure in a declarative manner, ensuring consistency across different environments.
 * Ansible: Ansible is a configuration management and automation tool that simplifies the deployment and management of applications and infrastructure. We use Ansible to automate tasks such as configuration, software installation, and orchestration of infrastructure components.
 * Docker: Docker is a containerization platform that enables the packaging of applications and their dependencies into containers. We use Docker to create lightweight, portable, and consistent environments, improving application consistency across various stages of the development lifecycle.
 * Kubernetes: Kubernetes is a container orchestration platform that automates the deployment, scaling, and management of containerized applications. We use Kubernetes to orchestrate and manage containers, ensuring high availability, scalability, and easy deployment of microservices.
 * Prometheus: Prometheus is an open-source monitoring and alerting toolkit designed for reliability and scalability. I use Prometheus to collect and store metrics from various components of the infrastructure, helping to monitor and troubleshoot issues proactively.
 * SonarQube: SonarQube is a platform for continuous inspection of code quality. We use SonarQube to perform static code analysis, identify and fix code quality issues, and ensure the overall health of the codebase.
 * Nexus: Nexus is a repository manager used to store and manage artifacts such as binary components and dependencies. We use Nexus to host and manage artifacts, ensuring a reliable and centralized repository for build artifacts and dependencies.
 ```

### 2. What are the main benefits of DevOps?
**A:**

```bash
DevOps is a very popular trend in Software Development. Some of the main benefits of DevOps are as follows:
I. Release Velocity: DevOps practices help in increasing the release velocity. We can release code to production more often and with more confidence.
II. Development Cycle: With DevOps, the complete Development cycle from initial design to production deployment becomes shorter.
III. Deployment Rollback: In DevOps, we plan for any failure in deployment rollback due to a bug in code or issue in production. This gives confidence in releasing feature without worrying about downtime for rollback.
IV. Defect Detection: With DevOps approach, we can catch defects much earlier than releasing to production. It improves the quality of the software.
V. Recovery from Failure: In case of a failure, we can recover very fast with DevOps process.
VI. Collaboration: With DevOps, collaboration between development and operations professionals increases.
VII. Performance-oriented: With DevOps, organization follows performance-oriented culture in which teams become more productive and more innovative.
```
### 3. What is the typical DevOps workflow you use in your organization?
**A:**

```bash
The typical DevOps workflow in our organization is as follows:
I. We use Allassian Jira for writing requirements and tracking tasks.
II. Based on the Jira tasks, developers checkin code into GIT version control system.
III. The code checked into GIT is built by using Apache Maven.
IV. The build process is automated with Jenkins.
V. During the build process, automated tests run to validate the code checked in by developer.
VI. Code built on Jenkins is sent to organization's Artifactory.
VII. Jenkins automatically picks the libraries from Artifactory and deploys it to Production.
VIII. During Production deployment Docker images are used to deploy same code on multiple hosts.
IX. Once code is deployed to Production, we use Nagios to monitor the health of production servers.
X. Splunk based alerts inform us of any issues or exceptions in production.
```
### 4. How do you take the DevOps approach with Amazon Web Services?
**A:**

```bash
Amazon Web Services (AWS) provide many tools and features to deploy and manage applications in AWS. As per DevOps, we treat infrastructure as code. We mainly use following two services from AWS for DevOps:
I. CloudFormation: We use AWS CloudFormation to create and deploy AWS resources by using templates. We can describe our dependencies and pass special parameters in these templates. CloudFormation can read these templates and deploy the application and resources in AWS cloud.
II. OpsWorks: AWS provides another service called OpsWorks that is used for configuration management by utilizing Chef framework. We can automate server configuration, deployment and management by using OpsWorks. It helps in managing EC2 instances in AWS as well as any on-premises servers.
```
### 5. How will you run a script automatically when a developer commits a change into GIT?
**A:**

```bash
GIT provides the feature to execute custom scripts when certain event occurs in GIT. This feature is called hooks.
We can write two types of hooks.
I. Client-side hooks
II. Server-side hooks
For this case, we can write a Client-side post-commit hook. This hook will execute a custom script in which we can add the message and code that we want to run automatically with each commit.
```
### 6. What are the main features of AWS OpsWorks Stacks?
**A:**

```bash
Some of the main features of AWS OpsWorks Stacks are as follows:
I. Server Support: AWS OpsWorks Stacks we can automate operational tasks on any server in AWS as well as our own data center.
II. Scalable Automation: We get automated scaling support with AWS OpsWorks Stacks. Each new instance in AWS can read configuration from OpsWorks. It can even respond to system events in the same way as other instances do.
III. Dashboard: We can create dashboards in OpsWorks to display the status of all the stacks in AWS.
IV. Configuration as Code: AWS OpsWorks Stacks are built on the principle of "Configuration as Code". We can define and maintain configurations like application source code. Same configuration can be replicated on multiple servers and environments.
V. Application Support: OpsWorks supports almost all kinds of applications. So it is universal in nature.
```
### 7. How does CloudFormation work in AWS?
**A:**

```bash
AWS CloudFormation is used for deploying AWS resources. In CloudFormation, we have to first create a template for a resource. A template is a simple text file that contains information about a stack on AWS. A stack is a collection of AWS resources that we want to deploy together in an AWS as a group. Once the template is ready and submitted to AWS, CloudFormation will create all the resources in the template. This helps in automation of building new environments in AWS.
```
### 8. What is CICD in DevOps?
**A:**

```bash
CICD stands for Continuous Integration and Continuous Delivery. These are two different concepts that are complementary to each other.
Continuous Integration (CI): In CI all the developer work is merged to the main branch several times a day. This helps in reducing integration problems. In CI we try to minimise the duration for which a branch remains checked out. A developer gets early feedback on the new code added to the main repository by using CI.
Continuous Delivery (CD): In CD, a software team plans to deliver software in short cycles. They perform development, testing and release in such a short time that incremental changes can be easily delivered to production.
In CD, as a DevOps we create a repeatable deployment process that can help achieve the objective of Continuous Delivery.
```
### 9. What are the best practices of Continuous Integration (CI)?
**A:**

```bash
Some of the best practices of Continuous Integration (CI) are as follows:
I. Build Automation: In CI, we create such a build environment that even with one command build can be triggered. This automation is done all the way up to deployment to the Production environment.
II. Main Code Repository: In CI, we maintain a main branch in the code repository that stores all the Production ready code. This is the branch that we can deploy to Production any time.
III. Self-testing build: Every build in CI should be self-tested. It means with every build there is a set of tests that runs to ensure that changes are of high quality.
IV. Every day commits to baseline: Developers will commit all of their changes to baseline everyday. This ensures that there is no big pileup of code waiting for integration with the main repository for a long time.
V. Build every commit to baseline: With Automated Continuous Integration, every time a commit is made into baseline, a build is triggered. This helps in confirming that every change integrates correctly.
VI. Fast Build Process: One of the requirements of CI is to keep the build process fast so that we can quickly identify any problem.
VII. Production like environment testing: In CI, we maintain a production like environment also known as pre production or staging environment, which is very close to Production environment. We perform testing in this environment to check for any integration issues.
VIII. Publish Build Results: We publish build results on a common site so that everyone can see these and take corrective actions.
IX. Deployment Automation: The deployment process is automated to the extent that in a build process we can add the step of deploying the code to a test environment. In this test environment all the stakeholders can access and test the latest delivery.
```
### 10. What are the benefits of Continuous Integration (CI)?
**A:**

```bash
The benefits of Continuous Integration (CI) are as follows:
I. CI makes the current build constantly available for testing, demo and release purposes.
II. With CI, developers write modular code that works well with frequent code check-ins.
III. In case of a unittest failure or bug, developers can easily revert back to the bug-free state of the code.
IV. There is drastic reduction in chaos on release day with CI practices.
V. With CI, we can detect Integration issues much earlier in the process.
VI. Automated testing is one very useful side effect of implementing CI.
VII. All the stakeholders including business partners can see the small changes deployed into the pre-production environment. This provides early feedback on the changes to software.
VIII. Automated CI and testing generates metrics like code-coverage, code complexity that help in improving the development process.
```
### 11. What are the options for security in Jenkins?
**A:**

```bash
In Jenkins, it is very important to make the system secure by setting user authentication and authorization. To do this we have to do following:
I. First we have to set up the Security Realm. We can integrate Jenkins with LDAP server to create user authentication.
II. Second part is to set the authorization for users. This determines which user has access to what resources.
In Jenkins some of the options to setup security are as follows:
I. We can use Jenkins' own User Database.
II. We can use LDAP plugin to integrate Jenkins with LDAP server.
III. We can also setup Matrix based security on Jenkins.
```
### 12. What are the main benefits of Ansible?
**A:**

```bash
Ansible is a powerful tool for IT Automation for large scale and complex deployments. It increases the productivity of team. Some of the main benefits of Ansible are as follows:
I. Productivity: It helps in delivering and deploying with speed. It increases productivity in an organisation.
II. Automation: Ansible provides very good options for automation. With automation, people can focus on delivering smart solutions.
III. Large-scale: Ansible can be used in small as well as very large-scale organisations.
IV. Simple DevOps: With Ansible, we can write automation in a human-readable language. This simplifies the task of DevOps.
```
### 13. What are the main use cases of Ansible?
**A:**

```bash
Some of the popular use cases of Ansible are as follows:
I. App Deployment: With Ansible, we can deploy apps in a reliable and repeatable way.
II. Configuration Management: Ansible supports the automation of configuration management across multiple environments.
III. Continuous Delivery: We can release updates with zero downtime with Ansible.
IV. Security: We can implement complex security policies with Ansible.
V. Compliance: Ansible helps in verifying an organisation's systems in comparison with the rules and regulations.
VI. Provisioning: We can provide new systems and resources to other users with Ansible.
VII. Orchestration: Ansible can be used in orchestration of complex deployment in a simple way.
```
### 14. What is Docker Hub?
**A:**

```bash
Docker Hub is a cloud-based registry. We can use Docker Hub to link code repositories. We can even build images and store them in Docker Hub. It also provides links to Docker Cloud to deploy the images to our hosts. Docker Hub is a central repository for container image discovery, distribution, change management, workflow automation and team collaboration.
```
### 15. What is your favourite scripting language for DevOps?
**A:**

```bash
In DevOps, we use different scripting languages for different purposes. There is no single language that can work in all the scenarios. Some of the popular scripting languages that we use are as follows:
I. Bash: On Unix based systems we use Bash shell scripting for automating tasks.
II. Python: For complicated programming and large modules we use Python. We can easily use a wide variety of standard libraries with Python.
III. Groovy: This is a Java based scripting language. We need JVM installed in an environment to use Groovy. It is very powerful and it provides very powerful features.
IV. Perl: This is another language that is very useful for text parsing. We use it in web applications.
```
### 16. What is Multi-factor authentication?
**A:**

```bash
In security implementation, we use Multi-factor authentication (MFA). In MFA, a user is authenticated by multiple means before giving access to a resource or service. It is different from simple user/password based authentication. The most popular implementation of MFA is Two-factor authentication. In most of the organisations, we use username/password and an RSA token as two factors for authentication. With MFA, the system becomes more secure and it cannot be easily hacked.
```
### 17. What is the use of Kubernetes?
**A:**

```bash
We use Kubernetes for automation of large-scale deployment of Containerized applications.
It is an open source system based on concepts similar to Google's deployment process of millions of containers. It can be used on cloud, on-premise datacenter and hybrid infrastructure.
In Kubernetes we can create a cluster of servers that are connected to work as a single unit. We can deploy a containerized application to all the servers in a cluster without specifying the machine name. We have to package applications in such a way that they do not depend on a specific host.
```
### 18.what is the difference between conatiner and virtual mission ?
**A:**

```bash
Virtual Machine: Runs a full OS on virtual hardware, so it is heavy and slow.

Container: Runs apps by sharing the host OS, so it is lightweight and fast.

Key difference: VM = hardware virtualization, Container = OS-level virtualization.
```