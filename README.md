# AWS DevOps Essentials
### Note that this lab guide is meant for AWS Lab Accounts, please follow [this lab guide](https://github.com/awslabs/aws-devops-essential) if you are using your own AWS account
### IMPORTANT: Please kindy read the section on Prerequisites - Lab Environment before starting the lab.

## An Introductory Workshop on CI/CD Practices

In few hours, quickly learn how to effectively leverage various AWS services to improve developer productivity and reduce the overall time to market for new product capabilities. In this session, we will demonstrate a prescriptive approach to incrementally adopt and embrace some of the best practices around continuous integration & delivery using AWS Developer Tools and 3rd party solutions including, AWS CodeCommit (a managed source control service), AWS CodeBuild (a fully managed build service), Jenkins (an open source automated build server), CodePipeline (a fully managed continuous delivery service), and CodeDeploy (an automated application deployment service). We will also highlight some best practices and productivity tips that can help make your software release process fast, automated, and reliable.

See the diagram below for a depiction of the complete architecture.

![DevOps Workshop Architecture](img/CICD_DevOps_Demo.png)

## Prerequisites - Lab Environment
          
**IAM Permissions:** 
As the AWS accounts you are about to use are Lab accounts, they do not have permissions to make any changes to IAM settings.
For any commands/steps that requires IAM Role ARN, please kindly use the pre-created role: **Team Role** .

https://console.aws.amazon.com/iam/home?region=ap-southeast-1#/roles/TeamRole

***It will be useful to note down the ARN for Team Role which will be required throughout the lab***

**Getting TeamRole ARN via console:**
```console
user:~/environment/ (master) $ aws iam get-role --role-name TeamRole
```
Note down the "ARN" portion of the JSON output.
***

### **Important:**
Preferred regions for lab
- Singapore: ap-southeast-1

If you want to use your region choice for the lab. Kindly the select the region which has all four Code* services and Cloud9 service. You can find the [region services list](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/). Stick to the same region throughout all labs. 
**Make sure you have not reached the VPC or Internet Gateway limits for that region. If you already have 5 VPCs/IGWs, delete at least one before you proceed or choose an alternate region.** 

# Labs
This workshop is broken into multiple labs. You must complete each Lab before proceeding to the next.

1. [Lab 1 - Build project on the cloud](1_Lab1.md) 
2. [Lab 2 - Automate deployment for testing](2_Lab2.md)
3. [Lab 3 - Setup CI/CD using AWS CodePipeline](3_Lab3.md)

## Clean up

1. Visit [CodePipeline console,](https://console.aws.amazon.com/codepipeline/home) select the created pipeline. Select the Edit and click **Delete**.
2. Visit [CodeDeploy console,](https://console.aws.amazon.com/codedeploy/home) select the created application. In the next page, click **Delete Application**.
3. Visit [CodeBuild console,](https://console.aws.amazon.com/codebuild/home) select the created project. Select the Action and click **Delete**.
4. Visit [CodeCommit console,](https://console.aws.amazon.com/codecommit/home) select the created repository. Go to setting and click **Delete repository**.
5. Visit [Lambda console,](https://console.aws.amazon.com/lambda/home) select the created function. Select the Action and click **Delete**.
6. Visit [Cloudformation console,](https://console.aws.amazon.com/cloudformation/home) select the created stacks. Select the Action and click **Delete Stack**.
7. Visit [Cloud9 console,](https://console.aws.amazon.com/cloud9/home) select the created Environment. Select the Action and click **Delete**.
8. Visit [Simple Notification Service console,](https://console.aws.amazon.com/sns/home) select Topics. Select the created topic.  Select the Action and click **Delete topics**. Next select Subscriptions. Select the created subscription. Select the Action and click **Delete subscriptions**.

## License

This library is licensed under the Apache 2.0 License. 
