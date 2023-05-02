# DevOps Exercise
```
TIMEBOX:    2-3 hours max. We mean it!
LANGUAGES:  HCL
TESTS:      plan file
DOCS:       infra diagram is nice to have, but not mandatory
```

# Overview
- This exercise is to implement the best possible solution to below exercises in the time alloted. We're evaluating your ability to take a set of requirements and spike a holistic solution that demonstrates craftsmanship, thoughtfulness and attention to user experience. 
- This is **NOT** a test of how well you know IaC, nor should you try to impress us with overly clever and obtuse solutions. If you want to impress us, build something that is beautiful, intuitive and easy to debug/test/extend :smiley: .
- Ideally your solution would have some way to run locally and visualize the results in a plan file so we can fully analyze the experience and not just the source code.

# Task
- You have been tasked with creating an infrastructure for website in AWS. This web application will be available to external users on the public Internet.
- Using HashiCorp's Terraform, create all required objects to fulfill the requirements to provide external access and ensure availability. 
- This can be contained in a single .tf file or structured in any way that you think would aid debugging or utilize best practices for structuring the configurations. 

# Requirements
1. Only the us-east-1 region is available
2. Use Ubuntu v18 AMI for webserver OS
3. Utilize the micro instance type
4. Create an auto-scaling group with a min/max size of 3/5
5. Expose the server externally such that only ingress traffic on port 80/443 is allowed. Egress traffic is unrestricted.
6. Create user-based S3 role that provides read/write access to a specific S3 bucket named s3-bucket

# Bonus
Answer following -
1. Manage tf state remotely in S3 bucket created
2. What terraform changes are needed to gracefully change the instance type from t2.micro to t2.small if the instances are already running? Please draft the changes in another branch.

# Submitting your exercise
1. See [instructions for submitting your work](https://github.com/prowerse-tech/jamming-opps#general-instructions)
