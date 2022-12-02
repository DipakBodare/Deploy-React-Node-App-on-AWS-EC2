#  Create EC2 ( Ubuntu Server ) instance

# Pre-requisities:
  Before creating EC2 instance, you have to check these major points which is as below.
  
- Choose AWS Region for your application ( for e.g Mumbai (ap-south-1), N.Virginia (us-east-1))
- Choose correct instance type ( for e.g t2.micro, t2.medium etc)
- Storage (How much storge required for your application? ) 
- Select the instance type (Linux server or windows server)
- Cost of instance type
- Create the Cost estimation of EC2 instance as well as your total applicaiton.

# AWS Cost Calculator URL link:
  By using aws cost calculator, your can create monthly as well as anually cost of your application.
  You can download these report in .pdf or .csv format
```
https://calculator.aws/#/
``


# EC2 security best practices

- Use only required inbound ports in security group.
- Enable linux firewall if you use linux system (optional)
- Enable EC2 AMI instance lifecycle policy (Take the AMI of server on daily or weekly basis)
- Assign Elastic Ip address to the server ( To avoid the IP address change after server shutdown)
- Assign EC2 access to authorized IAM user with specific permissions 
- Regularly patch, update and secure the operating system.
- You can use Amazon inspector to automatically discover and scan EC2 instances for software vulnerabilities and unintended network exposure.


