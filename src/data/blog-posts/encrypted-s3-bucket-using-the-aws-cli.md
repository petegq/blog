---
title: Encrypted S3 bucket using the AWS CLI
publishDate: 14 May 2023
description: Steps to create an encrypted S3 bucket using the AWS CLI.
---

**Steps to create an encrypted S3 bucket using the AWS CLI:**

1.  Open up your terminal or command prompt and make sure you have the AWS CLI installed and configured with your credentials.
2.  Run the following command to create a new S3 bucket:

```shell
aws s3api create-bucket --bucket <bucket-name> --region <region> --create-bucket-configuration LocationConstraint=<region>
```

Note: Replace `<bucket-name>` with your bucket name and `<region>` with the region you want to create the bucket in.

3.  Run the following command to enable default encryption for the bucket:

```shell
aws s3api put-bucket-encryption --bucket <bucket-name> --server-side-encryption-configuration '{"Rules":[{"ApplyServerSideEncryptionByDefault":{"SSEAlgorithm":"AES256"}}]}'
```

4.  Your bucket is now encrypted with AES256 encryption. You can verify this by running the following command:

```shell
aws s3api get-bucket-encryption --bucket <bucket-name>
```

Thats it! Your S3 bucket is now encrypted with default server-side encryption using AES256.
