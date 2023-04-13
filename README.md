# Build machine learning-ready datasets from the Offline Feature Store using the Amazon SageMaker Python SDK

## Introduction
Feature Store [extended the SageMaker Python SDK](https://docs.aws.amazon.com/sagemaker/latest/dg/feature-store-create-a-dataset.html) to make it easier to create datasets from the offline store. With this release, customers can use a new set of methods in the SDK to create datasets without writing SQL queries. These new methods support common operations such as time travel, filtering duplicate records, and joining multiple feature groups while ensuring point-in-time accuracy. 

In this repository, we will demonstrate how to use the SageMaker Python SDK to build machine learning-ready datasets without writing any SQL statements.

## Quick Start Guide
### Prerequisites

The code and the notebooks used in this repository were tested using [Amazon SageMaker](https://aws.amazon.com/sagemaker/). For best experience, we highly recommend using [SageMaker Studio](https://aws.amazon.com/sagemaker/studio/) or [SageMaker Notebook instances](https://docs.aws.amazon.com/sagemaker/latest/dg/nbi.html). 

If this is your first time using Amazon SageMaker, here's a good [starting point](https://docs.aws.amazon.com/sagemaker/latest/dg/gs-set-up.html) on setting up the SageMaker environment.

This project integrates with other AWS services, including S3, SageMaker Feature Store and Athena to provide examples. When configuring access control through IAM policies, we recommend getting started with the AWS managed policies, and move towards the least privilege permissions as a best practice.

Here're a list of Managed IAM Policies to associate with the SageMaker Execution Role: 
* [AmazonSageMakerFullAccess](https://docs.aws.amazon.com/sagemaker/latest/dg/security-iam-awsmanpol.html#security-iam-awsmanpol-AmazonSageMakerFullAccess)
* [AmazonSageMakerFeatureStoreAccess](https://docs.aws.amazon.com/sagemaker/latest/dg/security-iam-awsmanpol-feature-store.html#security-iam-awsmanpol-AmazonSageMakerFeatureStoreAccess)

Please refer to the following [IAM policy examples](https://docs.aws.amazon.com/sagemaker/latest/dg/security_iam_id-based-policy-examples.html) for additional customizations that provide finer grained permissions that meet your security requirements.

### Starting Point
To get started, you need to clone the project into your SageMaker Studio or Notebook environment and [run sagemaker-feature-store-offline-sdk notebook](sagemaker-feature-store-offline-sdk.ipynb).