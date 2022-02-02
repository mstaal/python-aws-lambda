# python-aws-lambda
Python 'Hello World' lambda function with Github Action workflow for AWS deployment

## Introduction
This is a very sparse and simple 'Hello World' sample showing how to make a Github Actions based workflow that automatically deploys a Python script as an AWS Lambda function.

## How to use it
Make an AWS IAM user with sufficient 'Permissions policies'. The user should be made with 'AWS_ACCESS_KEY_ID' and 'AWS_SECRET_ACCESS_KEY' based credentials. Make sure to note these credentials and add them as Github secrets in your repository. Adjust the 'AWS_REGION' environment variable in ´.github/workflows/pipeline.yml´ if you wish to use a different AWS region. One may alter or add function names in the ´strategy.matrix.function-name´ array in order to deploy multiple functions. There should always be a folder corresponding to each function, and the folder should have the same name as the corresponding function. The AWS Lambda function (with the same name) should first be specified inside of AWS, after which this workflow can then update the function.

## Acknowledgements
This sample is based on input from the following sources:
- https://docs.aws.amazon.com/lambda/latest/dg/python-package.html
- https://towardsaws.com/how-to-deploy-a-lambda-function-using-github-actions-nodejs-dfc8102ca70 (originally for Node.js)
