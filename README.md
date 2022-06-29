# IoT-Device-OTA-CICD-GitFlow

This repository provides an reference solution shows you how to deploy a continuous integration / continuous delivery (CI/CD) IoT device OTA deployment pipeline using AWS DevOps tools. Also will present a multi-branch solution for automated pipelines creation in AWS CodePipeline when a new branch is created in an AWS CodeCommit repository. The strategy presented here is to make your IoT device firmware development follow the GitFlow approach using only AWS tools.

# Solution Architecture

* Leverage AWS DevOps tools  CodeCommit, CodeBuild, CodePipeline as a CI/CD solution.
* Use AWS Signer to sign the firmware with ECDSA to guarantee the integrity and trusted author verification.
* Leverage Amazon S3 to store the firmware image and S3 Event Notifications for new image available,  use AWS Lambda to create IoT Jobs for OTA update, and use IoT rules to notify the OTA update status.
* Multi-branch CodePipeline strategy follow GitFlow approach in Firmware development.

The Detailed setup steps you can reference APG pattern [Deploy IoT Device OTA CICD Pipeline using AWS DevOps Tools](https://apg-library.amazonaws.com/content-viewer/author/430c89e4-eb00-4318-9b0c-d49b7f4a8113) 

# License
This library is licensed under the Amazon Software License, see License file
