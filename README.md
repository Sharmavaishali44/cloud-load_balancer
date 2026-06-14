#### &#x20; ***AWS Auto Scaling and Load Balancer Project***



* ##### ***Project Overview-***



***This project demonstrates how to manage and maintain web server traffic using an AWS Application Load Balancer (ALB) and Auto Scaling Group (ASG).***



***The Auto Scaling Group automatically launches additional EC2 instances when CPU utilization increases and terminates them when the load decreases. The Load Balancer distributes incoming traffic across healthy instances.***





* ##### &#x20;***Architecture-***

***(architecture.png)***





* ##### &#x20;***AWS Services Used***



***\* Amazon EC2***

***\* Launch Template***

***\* Auto Scaling Group (ASG)***

***\* Application Load Balancer (ALB)***

***\* Target Group***

***\* Amazon CloudWatch***







* ##### &#x20;***Project Workflow***



***1. Created a Launch Template.***

***2. Created an Auto Scaling Group.***

***3. Configured Minimum, Desired and Maximum Capacity.***

***4. Created an Application Load Balancer.***

***5. Attached Target Group to Auto Scaling Group.***

***6. Monitored CPU Utilization using CloudWatch.***

***7. Generated CPU load on EC2 instances.***

***8. Verified automatic instance scaling.***

##### 

* ##### ***Screenshots***



1. &#x20;***Launch Template***



***This launch template was used to define the EC2 instance configuration, including AMI, instance type, security group, and user data script.***



***2. Auto Scaling Group***



***The Auto Scaling Group was configured with minimum, desired, and maximum capacity to automatically manage EC2 instances based on workload.***



***3. Load Balancer***



***The Application Load Balancer distributes incoming traffic across healthy EC2 instances to improve availability and reliability.***



***4. Target Group***



***The target group contains the EC2 instances registered behind the load balancer and performs health checks on them.***







***5.  CPU Utilization***



***CPU load was generated on the EC2 instance to test the auto scaling functionality and trigger scaling actions.***







***6. Auto Scaled Instance***



***A new EC2 instance was automatically launched when CPU utilization exceeded the configured threshold.***





* ##### &#x20;***User Data Script***



***The user-data file is a script which was used to automatically install and configure the Apache web server during instance launch.***



* ##### ***Testing Commands***



***bash***

***systemctl status httpd (# if it shows in active then systemctl start httpd).***

***top***

***sha1sum /dev/zero***



* ##### ***Result***



***The Application Load Balancer successfully distributed traffic across EC2 instances, and the Auto Scaling Group automatically launched additional instances when CPU utilization crossed the configured threshold.***

