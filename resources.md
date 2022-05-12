---
description: >-
  The following resources were used in generating the presentation & demo for
  South Dakota Code Camp 2019.
---

# Resources

### Configuration Steps

Brief list of accounts and tools required for demo recreation

* GitLab Account
  * Public or Private _**Repo**_
  * Properly configured _**gitlab-ci.yml**_ file in repo.
  * Configured CI/CD _**AWS Environment Variables**_ (if using IAM Token)
  * (optional) _**GitLab Runner**_ deployed to AWS Account
* AWS Account
  * Can leverage 'free tier' resources
  * _**IAM User**_ (with Admin Permission for demoing)
    * [Template to deploy properly configured IAM User linked below](https://s3.us-east-2.amazonaws.com/aws-resources.tactfulcloud.com/iam/user-git-to-s3-ci.yml)
  * _**S3 Bucket**_ (Open to Public for Demo)
    * [Template to deploy properly configured S3 bucket linked below](https://s3.us-east-2.amazonaws.com/aws-resources.tactfulcloud.com/s3/bucket-resources-public.yml)
  * [Template to deploy Combination CI/CD IAM User & S3 Bucket linked below](https://s3.us-east-2.amazonaws.com/aws-resources.tactfulcloud.com/solutions/cicd-bucket-and-user.yml)

### Presentation

_**{Everything}-as-Code - An introduction to managing multiple AWS Accounts with Infrastructure-as-Code and CICD**_

### Docs

Links to docs for more detail on configuration

#### GitLab

* GitLab-CI Creation - [https://docs.gitlab.com/ee/ci/yaml/](https://docs.gitlab.com/ee/ci/yaml/)
* GitLab Typed AWS Variables - [https://gitlab.com/gitlab-org/gitlab-foss/issues/57780](https://gitlab.com/gitlab-org/gitlab-foss/issues/57780)
* GitLab Runner Configuration - [https://docs.gitlab.com/runner/](https://docs.gitlab.com/runner/)

#### AWS

* AWS Multiple Account Security Strategy  - [https://d0.awsstatic.com/aws-answers/AWS\_Multi\_Account\_Security\_Strategy.pdf](https://d0.awsstatic.com/aws-answers/AWS\_Multi\_Account\_Security\_Strategy.pdf)
* AWS Well-Architected Framework - [https://d1.awsstatic.com/whitepapers/architecture/AWS\_Well-Architected\_Framework.pdf](https://d1.awsstatic.com/whitepapers/architecture/AWS\_Well-Architected\_Framework.pdf)
* IAM User Creation - [https://docs.aws.amazon.com/IAM/latest/UserGuide/id\_users\_create.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id\_users\_create.html)
* Public S3 Bucket Creation - [https://docs.aws.amazon.com/AmazonS3/latest/user-guide/create-bucket.html](https://docs.aws.amazon.com/AmazonS3/latest/user-guide/create-bucket.html)

### Code

Public Cloudformation Templates (CFTs) and other resources

#### Project Demo

Demo GitLab Project - [https://gitlab.com/TactfulCloud/demos/change-control/sdcc2019](https://gitlab.com/TactfulCloud/demos/change-control/sdcc2019)

_**While logged into AWS:**_

* CFT for IAM User creation - [https://gitlab.com/TactfulCloud/AWS/aws-base-resources/blob/master/iam/user-git-to-s3-ci.yml](https://gitlab.com/TactfulCloud/AWS/aws-base-resources/blob/master/iam/user-git-to-s3-ci.yml)
  * _****_[_**Click Here to Deploy Stack in AWS**_](https://us-west-2.console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/create/review?templateURL=https://s3.us-east-2.amazonaws.com/aws-resources.tactfulcloud.com/iam/user-git-to-s3-ci.yml\&stackName=SDCC2019-CICD-IAM-User)_****_
* CFT for S3 Bucket creation - [https://gitlab.com/TactfulCloud/AWS/aws-base-resources/blob/master/s3/bucket-resources-public.yml](https://gitlab.com/TactfulCloud/AWS/aws-base-resources/blob/master/s3/bucket-resources-public.yml)
  * _****_[_**Click Here to Deploy Stack in AWS**_](https://us-west-2.console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/create/review?templateURL=https://s3.us-east-2.amazonaws.com/aws-resources.tactfulcloud.com/s3/bucket-resources-public.yml\&stackName=SDCC2019-CICD-Public-S3-Bucket)_****_
* CFT for combined CI/CD User/Bucket configuration - [https://gitlab.com/TactfulCloud/AWS/aws-base-resources/blob/master/solutions/cicd-bucket-and-user.yml](https://gitlab.com/TactfulCloud/AWS/aws-base-resources/blob/master/solutions/cicd-bucket-and-user.yml)
  * _****_[_**Click Here to Deploy Stack in AWS**_](https://us-west-2.console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/create/review?templateURL=https://s3.us-east-2.amazonaws.com/aws-resources.tactfulcloud.com/solutions/cicd-bucket-and-user.yml\&stackName=SDCC2019-CICD-User-Bucket)_****_
* Watch [_**here**_](https://gitlab.com/TactfulCloud/AWS/aws-base-resources) for other AWS Resources - [https://gitlab.com/TactfulCloud/AWS/aws-base-resources](https://gitlab.com/TactfulCloud/AWS/aws-base-resources)

_Default Scaffolding for building out AWS CI/CD Repo -_ [_https://gitlab.com/TactfulCloud/AWS/aws-ccm-master_](https://gitlab.com/TactfulCloud/AWS/aws-ccm-master)__

#### Libraries

* JSON Lint - [https://json-spec.readthedocs.io/](https://json-spec.readthedocs.io)
* YAML Lint - [https://yamllint.readthedocs.io/en/stable/quickstart.html](https://yamllint.readthedocs.io/en/stable/quickstart.html)
* CFN-NAG - [https://github.com/stelligent/cfn\_nag](https://github.com/stelligent/cfn\_nag)&#x20;

#### Container

* Docker File - [https://gitlab.com/TactfulCloud/containers/aws-cicd/blob/master/dockerfile](https://gitlab.com/TactfulCloud/containers/aws-cicd/blob/master/dockerfile)
* Image - registry.gitlab.com/tactfulcloud/containers/aws-cicd:v0.1

### Advanced Configuration Resources

Compliments of great team at JHC Technology

[https://gitlab.com/jhctechnology/aws-cloudformation-utilities/awslint](https://gitlab.com/jhctechnology/aws-cloudformation-utilities/awslint)

__
