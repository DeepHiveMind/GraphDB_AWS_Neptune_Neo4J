# Create a New Neptune Environment
- Create a new Neptune cluster/instance.

Cloudformation stack template that is available here: 
https://docs.aws.amazon.com/neptune/latest/userguide/get-started-create-cluster.html


#### EC2 Instance creation as workstation to connect to Neptune

- Create a management EC2 instance to connect to Neptune for 
	- bulk loading the CSV data (from S3) 
	- querying the graph after the load process has completed.

https://docs.aws.amazon.com/neptune/latest/userguide/bulk-load-tutorial-IAM.html


After creating an instance in Amazon Elastic Compute Cloud (Amazon EC2), you can log into that instance using SSH and connect to a Amazon Neptune DB cluster.

In order for the Amazon EC2 instance to connect to your Neptune endpoint on, for example, port 8182, you will need to set up a security group to do that. If your Amazon EC2 instance is using a security group named, for example, ec2-sg1, you need to create another Amazon EC2 security group (let's say db-sg1) that has inbound rules for port 8182 and has ec2-sg1 as its source. Then, add db-sg1) to your Neptune cluster to allow the connection.


### Connect to Gremlin Console

Please refer to section
	- "To connect to Neptune using the Gremlin Console with Signature Version 4 signing"
of https://docs.aws.amazon.com/neptune/latest/userguide/iam-auth-connecting-gremlin-console.html


## get Started Neptune Reference

https://docs.aws.amazon.com/neptune/latest/userguide/get-started.html

