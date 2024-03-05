
```markdown
# Hosting a Static Website on AWS with CloudFormation

This project involves deploying a static HTML web application on AWS using CloudFormation. Below is an overview of the resources utilized and the steps taken to deploy the web app.

## Project Overview

The project utilizes various AWS services and configurations:

1. **Virtual Private Cloud (VPC)**:
   - Configured a VPC with public and private subnets across two availability zones for enhanced fault tolerance.

2. **Internet Gateway**:
   - Deployed an Internet Gateway to facilitate connectivity between VPC instances and the wider Internet.

3. **Security Groups**:
   - Established Security Groups as a network firewall mechanism for controlling inbound and outbound traffic.

4. **Availability Zones**:
   - Leveraged two Availability Zones to enhance system reliability and fault tolerance.

5. **Public and Private Subnets**:
   - Utilized Public Subnets for infrastructure components like the NAT Gateway and Application Load Balancer.
   - Positioned web servers (EC2 instances) within Private Subnets for enhanced security.

6. **NAT Gateway**:
   - Enabled instances in private subnets to access the Internet via the NAT Gateway.

7. **Hosting the Website on EC2 Instances**:
   - Deployed the static website on EC2 instances.

8. **Application Load Balancer (ALB)**:
   - Employed an Application Load Balancer and a target group for evenly distributing web traffic to an Auto Scaling Group of EC2 instances across multiple Availability Zones.

9. **Auto Scaling Group (ASG)**:
   - Utilized an Auto Scaling Group to automatically manage EC2 instances, ensuring website availability, scalability, fault tolerance, and elasticity.

10. **Version Control and Collaboration**:
    - Stored web files on GitHub for version control and collaboration.

11. **Certificate Manager**:
    - Secured application communications using a Certificate Manager.

12. **Simple Notification Service (SNS)**:
    - Configured SNS to alert about activities within the Auto Scaling Group.

13. **Domain Name and DNS Setup**:
    - Registered the domain name and set up a DNS record using Route 53.

## Deployment Instructions

1. **Clone the Repository**:
   - Clone the GitHub repository containing the CloudFormation scripts for deploying the web application.

2. **Update Parameters**:
   - Modify the parameters in the CloudFormation template according to your requirements, such as domain name, SSL certificate ARN, etc.

3. **Deploy the Stack**:
   - Use AWS CLI or AWS Management Console to deploy the CloudFormation stack.

4. **Upload Website Files**:
   - After stack creation, upload the static website files to the EC2 instances.

5. **Verify Deployment**:
   - Once the deployment is complete, verify the website's availability and functionality.

## Cleanup

- To avoid incurring unnecessary costs, delete the CloudFormation stack and associated resources after testing or when they are no longer needed.

## Additional Notes

- Ensure proper security configurations are in place to protect the resources.
- Monitor AWS usage to manage costs effectively.
- Regularly update and maintain the website and associated resources.

## Resources

- [AWS CloudFormation Documentation](https://docs.aws.amazon.com/cloudformation/)
- [AWS CLI Documentation](https://aws.amazon.com/cli/)
- [Amazon EC2 Documentation](https://docs.aws.amazon.com/ec2/)
- [Amazon VPC Documentation](https://docs.aws.amazon.com/vpc/)
- [Amazon Route 53 Documentation](https://docs.aws.amazon.com/route53/)
- [Amazon Certificate Manager Documentation](https://docs.aws.amazon.com/acm/)
- [Amazon SNS Documentation](https://docs.aws.amazon.com/sns/)
```

This README provides an overview of the project, deployment instructions, cleanup procedures, additional notes, and links to relevant AWS documentation for further reference. Adjust the instructions and details as needed based on your specific project setup and requirements.
