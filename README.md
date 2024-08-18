   ![image](https://github.com/user-attachments/assets/4c5d5f84-5063-43e6-8f91-912135abf6c7)

# Project:

- Design and configure a VPC: Create a VPC with custom IP ranges. Set up public and private subnets. Configure route tables and associate subnets.

- Implement network security: Set up network access control lists (ACLs) to control inbound and outbound traffic. Configure security groups for EC2 instances to allow specific ports and protocols.

- Provision EC2 instances: Launch EC2 instances in both the public and private subnets. Configure security groups for the instances to allow necessary traffic. Create and assign IAM roles to the instances with appropriate permissions.

- Networking and routing: Set up an internet gateway to allow internet access for instances in the public subnet. Configure NAT gateway or NAT instance to enable outbound internet access for instances in the private subnet. Create appropriate route tables and associate them with the subnets.

- SSH key pair and access control: Generate an SSH key pair and securely store the private key. Configure the instances to allow SSH access only with the generated key pair. Implement IAM policies and roles to control access and permissions to AWS resources.

- Test and validate the setup: SSH into the EC2 instances using the private key and verify connectivity. Test network connectivity between instances in different subnets. Validate security group rules and network ACL settings.

- By implementing this project, you'll gain hands-on experience in setting up a secure VPC with EC2 instances, implementing networking and routing, configuring security groups and IAM roles, and ensuring proper access control. This project will provide a practical understanding of how these AWS services work together to create a secure and scalable infrastructure for your applications.

## Now we can see the step by step process
   - ### creatoin of vpc.
     ![Screenshot 2024-08-18 163416](https://github.com/user-attachments/assets/c2e77e9a-45f4-47a9-9957-249b2bef6af1)

   - ### creatio of Auto Scaling Group.
     ![Screenshot 2024-08-18 185440](https://github.com/user-attachments/assets/179a59d3-3ffd-4b84-909c-61539504fd14)

   - After creation of auto scaling group,created two EC2 instance without public iP.
   - we manually create a EC2(Bastion-host) with enable public ip.
     ![Screenshot 2024-08-18 185535](https://github.com/user-attachments/assets/3b966eda-14fe-465f-9d6b-47c71917d181)
       
   - send .pem file into Bastion-host.
   - access other instance using.
   - ### **ssh -i < filename.pem > ubuntu @< private-ip >**.
     ![Screenshot (416)](https://github.com/user-attachments/assets/7607ee8d-c59f-46b4-844d-b26f93c351a8)
   
   - we create index.html with some data.
   - after use this command to run **python3 -m http.server 8000**.
   - last step, you need to create a load balancer.
     1. Target Group.
        -create target group with two instances except Bastion-host.
        ![Screenshot 2024-08-18 185516](https://github.com/user-attachments/assets/24828906-987e-4ecc-be45-968720562450)
     2. Load Balancer creation.
        ![Screenshot 2024-08-18 185457](https://github.com/user-attachments/assets/b840fc82-5fac-4be7-917a-2d33bd7e14da)




