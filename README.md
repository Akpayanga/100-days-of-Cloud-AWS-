# 100-days-of-Cloud-AWS-
This is my live portfolio for the **100 Days of Cloud** challenge.   I'm documenting each day's task with real AWS console screenshots.  I'll keep updating this README as I progress.

## Progress Overview
![Progress Overview](Screenshots/progress-overview.png)  

Completed all tasks up to Day 16. Below are the days I currently have screenshots for, shown in chronological order.

## Completed Tasks with Screenshots

### Day 3: Create Subnet
![Day 3 - Create Subnet](Screenshots/day-3-create-subnet.png)  

Created a new custom subnet (`devops-subnet`) in my VPC with CIDR 172.31.128.0/20.

**Learnings:** Subnets allow logical isolation of resources, control traffic flow, and placement in specific Availability Zones.

### Day 8: Enable Stop Protection for EC2 Instance
![Day 8 - Enable Stop Protection](Screenshots/day-8-stop-protection.png)  

Enabled stop protection on a running EC2 instance to prevent accidental stopping.

**Learnings:** Stop protection is a safeguard against unintended downtime caused by manual errors.

### Day 9: Enable Termination Protection for EC2 Instance
![Day 9 - Enable Termination Protection 1](Screenshots/day-9-termination-protection-1.png)  

Enabled termination (deletion) protection on running instances.

**Learnings:** Critical for production — prevents irreversible deletion of important instances.

### Day 10: Attach Elastic IP to EC2 Instance
![Day 10 - Attach Elastic IP](Screenshots/day-10-elastic-ip.png)  

Associated a static Elastic IP (98.86.35.126) with my EC2 instance.

**Learnings:** Elastic IPs provide a fixed public IP that remains even after stop/start cycles — great for production services.

### Day 11: Attach Elastic Network Interface to EC2 Instance
![Day 11 - Attach Network Interface](Screenshots/day-11-network-interface.png)  

Attached a secondary Elastic Network Interface (ENI) to the instance (noted t2.micro limitations on advanced features).

**Learnings:** ENIs enable multiple network connections per instance for advanced networking scenarios.

### Day 12: Attach Volume to EC2 Instance
![Day 12 - Attach Volume](Screenshots/day-12-attach-volume.png)  

Attached an additional EBS volume (`xfusion-volume`) to a running instance as `/dev/sdb`.

**Learnings:** You can expand storage on live instances without downtime.

### Day 13: Create AMI from EC2 Instance
![Day 13 - Create AMI](Screenshots/day-13-create-ami.png)  

Created a custom Amazon Machine Image (AMI) from a configured running instance.

**Learnings:** AMIs are reusable templates for launching identical, pre-configured instances quickly.

### Day 14: Terminate EC2 Instance
![Day 14 - Terminate Instance](Screenshots/day-14-terminate-instance.png)  

Safely terminated an instance after disabling protections (confirmed root volume deletion).

**Learnings:** Termination is permanent — always create AMIs or snapshots first for important data.

### Day 15: Create Volume Snapshot
![Day 15 - Create Snapshot](Screenshots/day-15-create-snapshot.png)  

Created a point-in-time snapshot of an EBS volume.

**Learnings:** Snapshots are incremental backups — cost-effective for data protection and recovery.

### Day 16: Create IAM User 
![Day 16 - IAM Password Settings](Screenshots/day-16-iam-password.png)  

Created a new IAM user (`iamuser_john`) with console access, auto-generated password, and forced password reset on first login.

**Learnings:** Never use the root account for daily tasks. Use IAM users with least privilege, enable MFA, and enforce strong password policies.

### Day 17 - Created an IAM Group.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/un0zpcdfnsn8e6s05fyd.png)

IAM Groups are containers that make it easier to manage permissions for multiple users at once. You attach policies to the group, then add users to it—so everyone in the group gets the same permissions without having to configure each user individually.
