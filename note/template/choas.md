
Stop one or more EC2 instances

Stop all EC2 Instances

Stop an ECS service by putting the number of tasks to be rotated at 0

Delete from an ECS cluster
  
Put a slow connection on proxy (check Network ACL rules)

Cut outflow through the proxy (/etc/hosts of the proxy, put an erroneous address for a given host, a partner for example)

Deletion of IAM Rules
     
Deletion of items in DynamoDB

Cut off access to the RDS base via IAM
    
Delete a file on S3
  
Stubborn issues of authentication, a name in space cause 403 request error.
           
Check for 
1. IAM (Identity and Access Management):
   - User names
   - Role names
   - Policy names or content

2. Amazon Cognito:
   - User pool names
   - Identity pool names
   - User attributes

3. AWS Security Token Service (STS):
   - Assumed role names
   - Session names

4. API Gateway:
   - API keys
   - Usage plan names
   - Resource policy

5. S3 (Simple Storage Service):
   - Bucket policy
   - IAM user or role specified in bucket policy

6. EC2 (Elastic Compute Cloud):
   - Instance profile names
   	  - Security group names

7. Lambda:
   - Function names
   - Execution role names

8. Application code:
   - Environment variables storing access keys or tokens
   - Configuration files with authentication information

9. AWS CLI or SDK configuration:
   - Profiles in ~/.aws/credentials or ~/.aws/config files

10. Systems Manager Parameter Store:
   - Parameter names storing sensitive information

Source: https://www.valeuriad.fr/chaos-engineering-sur-aws-faire-son-propre-gameday/

11. Security Group misconfigurations:
Required ports might not be allowed, blocking necessary traffic.

12.Routing table problems:
Incorrect or missing routing table assignments to subnets.
Inappropriate rules in the routing tables.

13. VPC and instance issues:
Instances might be down or not properly registered with the Auto Scaling group.

14. Subnet configuration problems:
Incorrect CIDR block size ("Subnet 'cider'???") might lead to IP address shortages.
Subnets might not be properly added to the Elastic Load Balancer or Auto Scaling Group.

15. Network ACL issues:
ACLs on subnets might be too restrictive or too permissive, causing security or connectivity problems.
16.Internet Gateway (IGW) connectivity:
Lack of proper routes to the IGW.

17.DNS issues:
Route53 records might be pointing to incorrect resources.
             
Source:https://github.com/fedorovdima/aws-gameday/blob/master/runbook.md