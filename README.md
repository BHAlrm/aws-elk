##Solution Overview
This solution use Amazon Cloudwatch log to collect and aggregate log from Amazon Lambda service which exposed by Amazon API gateway. It uses a CloudWatch Logs Subscription to deliver the log to Amazon Elasticsearch Service (Amazon ES) for analysis and visualization with Kibana.

This solution contains a test environment AWS CloudFormation stack that you can automatically provision into an existing Amazon VPC subnet. The CloudFormation template performs the following high-level steps in the region you choose:
- Creates One AWS API Gateway to be entry point for helloworld api
- Creates the Helloworld Lambda function
- Creates the Amazon ES domain.
- Creates the CloudWatch Logs group.
- Creates the Lambda function and CloudWatch Logs Subscription in order to send log to Amazon ES.
