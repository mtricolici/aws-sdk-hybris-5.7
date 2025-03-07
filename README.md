# AWS SDK for Java [![Build Status](https://travis-ci.org/aws/aws-sdk-java.png?branch=master)](https://travis-ci.org/aws/aws-sdk-java)

The **AWS SDK for Java** enables Java developers to easily work with [Amazon Web Services][aws] and build scalable solutions with Amazon S3, Amazon DynamoDB, Amazon Glacier, and more. You can get started in minutes using ***Maven*** or by downloading a [single zip file][install-jar].

* [API Docs][docs-api]
* [SDK Homepage][sdk-website]
* [Forum][sdk-forum]
* [Issues][sdk-issues]
* [SDK Blog][blog]
* [Developer Guide][docs-guide]

## Getting Started
#### Sign up for AWS ####
Before you begin, you need an AWS account. Please see the [AWS Account and Credentials][docs-signup] section of the developer guide for information about how to create an AWS account and retrieve your AWS credentials.

#### Minimum requirements ####
To run the SDK you will need **Java 1.6+**. For more information about the requirements and optimum settings for the SDK, please see the [Java Development Environment][docs-signup] section of the developer guide.

#### Install the SDK ####
The recommended way to use the AWS SDK for Java in your project is to consume it from Maven. Import the <a href="https://github.com/aws/aws-sdk-java/tree/master/aws-java-sdk-bom">aws-java-sdk-bom</a> and specify the SDK Maven modules your project needs in the dependencies.

##### Importing the BOM #####
```
<dependencyManagement>
  <dependencies>
    <dependency>
      <groupId>com.amazonaws</groupId>
      <artifactId>aws-java-sdk-bom</artifactId>
      <version>1.10.35</version>
      <type>pom</type>
      <scope>import</scope>
    </dependency>
  </dependencies>
</dependencyManagement>
```
##### Using the SDK Maven modules #####
``` 
<dependencies>
  <dependency>
    <groupId>com.amazonaws</groupId>
    <artifactId>aws-java-sdk-ec2</artifactId>
  </dependency>
  <dependency>
    <groupId>com.amazonaws</groupId>
    <artifactId>aws-java-sdk-s3</artifactId>
  </dependency>
  <dependency>
    <groupId>com.amazonaws</groupId>
    <artifactId>aws-java-sdk-dynamodb</artifactId>
  </dependency>
</dependencies>
```
   Please see the
   [Install the AWS SDK for Java][docs-signup] section of the user guide for more detailed information about installing the SDK through other means.

## Features

* Provides easy-to-use HTTP clients for all supported AWS services, regions, and authentication protocols.
* Client-Side Data Encryption for Amazon S3 - Helps improve the security of storing application data in Amazon S3.
* Amazon DynamoDB Object Mapper - Uses Plain Old Java Object (POJOs) to store and retrieve Amazon DynamoDB data.
* Amazon S3 Transfer Manager - With a simple API, achieve enhanced the throughput, performance, and reliability by using multi-threaded Amazon S3 multipart calls.
* Amazon SQS Client-Side Buffering - Collect and send SQS requests in asynchronous batches, improving application and network performance.
* Automatically uses [IAM Instance Profile Credentials][aws-iam-credentials] on configured Amazon EC2 instances.
* And more!

## Building From Source

Once you check out the code from GitHub, you can build it using Maven.  To disable the GPG-signing in the build, use: `mvn clean install -Dgpg.skip=true`

## Supported Versions

1.10.x - Recommended.
1.9.x - Approved. Only major critical bugs will be fixed. To get the new features, upgrade to 1.10.x version of the SDK.

[install-jar]: http://sdk-for-java.amazonwebservices.com/latest/aws-java-sdk.zip
[aws]: http://aws.amazon.com/
[sdk-website]: http://aws.amazon.com/sdkforjava
[sdk-forum]: http://developer.amazonwebservices.com/connect/forum.jspa?forumID=70
[sdk-issues]: https://github.com/aws/aws-sdk-java/issues
[sdk-license]: http://aws.amazon.com/apache2.0/
[docs-api]: http://docs.aws.amazon.com/AWSJavaSDK/latest/javadoc/index.html
[docs-signup]: http://docs.aws.amazon.com/AWSSdkDocsJava/latest/DeveloperGuide/java-dg-setup.html
[aws-iam-credentials]: http://docs.aws.amazon.com/AWSSdkDocsJava/latest/DeveloperGuide/java-dg-roles.html
[docs-guide]: http://docs.aws.amazon.com/AWSSdkDocsJava/latest/DeveloperGuide/welcome.html
[blog]: https://java.awsblog.com