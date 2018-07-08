# AWS Organizations

![alt](./images/organizations.png)

two types:
* all features (policies, etc)
* only consolidated billing

##  consolidated billing

- 20 linked accounts max (could be increased)
- one bill per AWS account
- east to track charges and allocate costs
- volume pricing discounts
- reserved EC2 instances (could use RI in other accounts)
- billing alerts are not available on linked accounts

Cloudtrail:
- per AWS account & is per region
- can consolidate logs using an S3 bucket

## Service Control Policies


## Cost Explorer

Cost Explorer tool which allows filter graphs by API operations, Availability Zones, AWS service, custom cost allocation tags, EC2 instance type, purchase options, region, usage type, usage type groups, or, if Consolidated Billing used, by linked account.

## Budgets

- Budgets can be used to track AWS costs to see usage-to-date and current estimated charges from AWS
- Budgets use the cost visualization provided by Cost Explorer to show the status of the budgets and to provide forecasts of your estimated costs.
- Budgets can be used to create CloudWatch alarms that notify when you go over your budgeted amounts, or when the estimated costs exceed budgets
- Notifications can be sent to an SNS topic and to email addresses associated with your budget notification

## Cost Allocation Tags

- Tags can be used to organize AWS resources, and cost allocation tags to track the AWS costs on a detailed level.
- Upon cost allocation tags activation, AWS uses the cost allocation tags to organize the resource costs on the cost allocation report making it easier to categorize and track your AWS costs.
- AWS provides two types of cost allocation tags,
    * an AWS-generated tag AWS defines, creates, and applies the AWS-generated tag for you,
    * and user-defined tags that you define, create,
- Both types of tags must be activated separately before they can appear in Cost Explorer or on a cost allocation report

Billing alerts must be enalbed manually first time to be able to create alarms