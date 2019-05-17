# What's this ?

This is AWS CloudFormation Template for API Documents from OpenAPI/Swagger 2.0 API specifications.
You can generate HTML documents on Amazon S3, and we can see that documents via CloudFront.

# How to use

1. Push your swagger files to Github repository.
2. Create stack with `api_docs.yml`.
3. Open CloudFront url with your browser.

If you need modify buildspec.yml for your swagger file.

# How it works

Generate html useing [Spectacle](https://github.com/sourcey/spectacle) on AWS CodeBuild.
CodeBuild is started by CodePipeline.
CodePipeline is started by Github Webhooks.

After generating documents, put html files to S3 bucket.
This S3 bucket is publish using CloudFront.

# Blog
https://dev.classmethod.jp/cloud/aws/swagger-api-docs…rmation-template/ ‎
