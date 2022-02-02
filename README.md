# python-aws-lambda
Python 'Hello World' lambda function with Github Action workflow for AWS deployment

## Introduction
This is a very sparse and simple 'Hello World' sample showing how to make a Github Actions based workflow that automatically deploys a Python script as an AWS Lambda function.

## How to use it
Make an AWS IAM user with sufficient 'Permissions policies'. The user should be made with 'AWS_ACCESS_KEY_ID' and 'AWS_SECRET_ACCESS_KEY' based credentials. Make sure to note these credentials and add them as Github secrets in your repository. Adjust the 'AWS_REGION' and 'FUNCTION_NAME' environment variables in ´.github/workflows/pipeline.yml´ if you wish to use a different AWS region or function name, respectively. If the function name is adjusted, the ´hello_world´ folder should be renamed accordingly. The AWS Lambda function (with the same name) should first be specified inside of AWS, after which this workflow can then update the function.
