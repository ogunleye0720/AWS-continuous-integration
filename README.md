# CONTINUOUS INTEGRATION PROJECT USING AWS CODEPIPELINE

![DEVOPS LOOP](images/Continuous_Integration.webp)

## INTRODUCTION
<p> Continuous Integration (CI) is a cornerstone practice in Agile development methodologies, revolutionizing the way software is built, tested, and delivered. In an era where software development cycles are increasingly demanding speed, flexibility, and quality, CI stands as a critical enabler of Agile principles. It's a powerful approach that promotes collaboration, ensures code stability, and accelerates the release of high-quality software.</p> 

<p>At its core, CI is a development practice that encourages team members to integrate their code frequently. It's more than just a technical process; it's a cultural shift in how software is crafted. With CI, developers no longer work in isolation on separate pieces of code for extended periods. Instead, they continuously merge their code into a shared repository, triggering automated builds and tests.</p>

<p>In this evolving landscape of software development, where customer needs and market dynamics changes rapidly, Continuous Integration acts as a bridge between code creation and value delivery. It promotes the principles of adaptability, customer-centricity, and incremental progress. By doing so, it's not just a practice; it's a fundamental driver of success in Agile development, ensuring that software remains a nimble, high-quality, and valuable asset in a constantly changing world.</p>

## AIM AND OBJECTIVES
### AIM
<P> The aim of this project is to utilise a cloud native solution towards improving software quality by automating test and validation processes.</P>

### OBJECTIVES
<p>The objectives of this project are: </p>

#

- To implement automated build and compilation processes, ensuring that code is built correctly and consistently.

- To automate the testing process, in order to validate code changes, including unit tests, integration tests, and end-to-end tests.

- To implement automated monitoring and alerts to detect and respond to issues quickly.

- To reduce manual intervention and errors in the software delivery process, making it more efficient and reliable.
- To incorporate security checks and testing into the CI/CD pipeline to identify and address security vulnerabilities early.

- To use AWS CodePipeline to optimize costs by minimizing the use of resources when not required.
  
- To facilitate the integration of various tools and services used in the development and deployment process, such as version control systems, testing frameworks, and cloud platforms.

# Technologies 
- Spring MVC
- Spring Security
- Spring Data JPA
- Maven 3 or later
- JSP
- JDK 8 (correto8) and JDK 11
- MySQL version 5.6 or later
- AWS CodePipeline
- AWS CodeCommit
- AWS CodeBuild
- Sonar Cloud
- AMAZON SNS
- S3 Bucket

# ARCHITECTURE OVERVIEW

- [x] AWS CodeCommit :- AWS CodeCommit is a fully managed source control service provided by Amazon Web Services (AWS). It is a version control service that makes it easy for teams to host secure and highly scalable Git repositories. Here are some key features and aspects of AWS CodeCommit. In this project, AWS CodeCommit was used to host the java applcation source control. This service offers a seamless integration with other AWS resources, which helps increase the speed and frequency of software development cycle.

- [x] AWS CodeArtifact :- AWS CodeArtifact is a fully managed software package repository service provided by Amazon Web Services (AWS). It is designed to help developers and organizations securely store, publish, and share software packages. AWS CodeArtifact serves as a central hub for managing dependencies, enabling teams to streamline their software development and deployment processes. In this project, the  CodeArtifact was used to store MVN package manager, which would be used during the build stage of the project.

- [x] AWS CodeBuild :- AWS CodeBuild is a fully managed continuous integration service, provided by Amazon Web Services (AWS). It is designed to help developers build, test, and package their code quickly and efficiently. AWS CodeBuild can be integrated into the software development workflow to automate the build and test phases. In this project, AWS codebuild was integrated with SonarQube, to perform code analysis, with Maven to perform unit test, checkstyle test and to build the code artifact, which was stored in an Amazon S3 bucket.

- [x] AWS CodePipeline :- AWS CodePipeline is a continuous integration and continuous delivery (CI/CD) service, provided by Amazon Web Services (AWS). It automates the build, test, and deployment phases of a software release process, enabling the delivery of software and updates more rapidly and reliably. AWS CodePipeline helps to streamline software delivery pipeline, from code changes to production deployments.

- [x] Amazon S3 :- Amazon S3 (Amazon Simple Storage Service) is an object storage service provided by Amazon Web Services (AWS). It is designed to store and retrieve any amount of data, from anywhere on the web. In this project, the Amazon S3 was used to store the Software dependencies, and artifacts after a successful build process. This dependencies stored in the S3 bucket, would later be referenced during the deploy stage of the pipeline to generate an artifact.

- [x] Amazon SNS :- Amazon Simple Notification Service (Amazon SNS) is a fully managed messaging service provided by Amazon Web Services (AWS). It allows send messages and notifications to be sent to a large number of recipients through various communication channels, such as email, SMS (Short Message Service), application endpoints (e.g., mobile devices), and even HTTP endpoints. In this project, the SNS was used to send information about the build and test stages success, failure, code changes, and process termination, to an administrative email.

- [x] Sonar Cloud :- SonarCloud is a cloud-based, software quality and security platform provided by SonarSource. It's designed to help development teams ensure the quality, maintainability, and security of their code throughout the software development lifecycle. SonarCloud is a part of the larger SonarQube ecosystem but is hosted and maintained by SonarSource, making it a convenient choice for teams looking for a cloud-based solution. In this project, SonarQube was used to perform code analysis test on the project source code.