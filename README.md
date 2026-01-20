# 100-days-of-Cloud-AWS-
This is my live portfolio for the **100 Days of Cloud** challenge.   I'm documenting each day's task with real AWS console screenshots.  I'll keep updating this README as I progress.

## Progress Overview
![Progress Overview](screenshots/progress-overview.png)  

Completed all tasks up to Day 16. Below are the days I currently have screenshots for, shown in chronological order.

## Completed Tasks with Screenshots

### Day 3: Create Subnet
![Day 3 - Create Subnet](screenshots/day-3-create-subnet.png)  

Created a new custom subnet (`devops-subnet`) in my VPC with CIDR 172.31.128.0/20.

**Learnings:** Subnets allow logical isolation of resources, control traffic flow, and placement in specific Availability Zones.

### Day 8: Enable Stop Protection for EC2 Instance
![Day 8 - Enable Stop Protection](screenshots/day-8-stop-protection.png)  

Enabled stop protection on a running EC2 instance to prevent accidental stopping.

**Learnings:** Stop protection is a safeguard against unintended downtime caused by manual errors.

### Day 9: Enable Termination Protection for EC2 Instance
![Day 9 - Enable Termination Protection 1](screenshots/day-9-termination-protection-1.png)  
![Day 9 - Enable Termination Protection 2](screenshots/day-9-termination-protection-2.png)  

Enabled termination (deletion) protection on running instances.

**Learnings:** Critical for production — prevents irreversible deletion of important instances.

### Day 10: Attach Elastic IP to EC2 Instance
![Day 10 - Attach Elastic IP](screenshots/day-10-elastic-ip.png)  

Associated a static Elastic IP (98.86.35.126) with my EC2 instance.

**Learnings:** Elastic IPs provide a fixed public IP that remains even after stop/start cycles — great for production services.

### Day 11: Attach Elastic Network Interface to EC2 Instance
![Day 11 - Attach Network Interface](screenshots/day-11-network-interface.png)  

Attached a secondary Elastic Network Interface (ENI) to the instance (noted t2.micro limitations on advanced features).

**Learnings:** ENIs enable multiple network connections per instance for advanced networking scenarios.

### Day 12: Attach Volume to EC2 Instance
![Day 12 - Attach Volume](screenshots/day-12-attach-volume.png)  

Attached an additional EBS volume (`xfusion-volume`) to a running instance as `/dev/sdb`.

**Learnings:** You can expand storage on live instances without downtime.

### Day 13: Create AMI from EC2 Instance
![Day 13 - Create AMI](screenshots/day-13-create-ami.png)  

Created a custom Amazon Machine Image (AMI) from a configured running instance.

**Learnings:** AMIs are reusable templates for launching identical, pre-configured instances quickly.

### Day 14: Terminate EC2 Instance
![Day 14 - Terminate Instance](screenshots/day-14-terminate-instance.png)  

Safely terminated an instance after disabling protections (confirmed root volume deletion).

**Learnings:** Termination is permanent — always create AMIs or snapshots first for important data.

### Day 15: Create Volume Snapshot
![Day 15 - Create Snapshot](screenshots/day-15-create-snapshot.png)  

Created a point-in-time snapshot of an EBS volume.

**Learnings:** Snapshots are incremental backups — cost-effective for data protection and recovery.

### Day 16: Create IAM User
![Day 16 - IAM User Details](screenshots/day-16-iam-details.png)  
![Day 16 - IAM Password Settings](screenshots/day-16-iam-password.png)  

Created a new IAM user (`iamuser_john`) with console access, auto-generated password, and forced password reset on first login.

**Learnings:** Never use the root account for daily tasks. Use IAM users with least privilege, enable MFA, and enforce strong password policies.

### Additional Screenshots: EC2 Exploration
![EC2 Dashboard](screenshots/ec2-dashboard.png)  
![EC2 Instances List](screenshots/ec2-instances-list.png)  

Viewed the EC2 dashboard (noted API errors from experimentation) and instance list (running + terminated instances).

**Learnings:** Monitoring resource usage and quotas is essential, especially on free tier.
