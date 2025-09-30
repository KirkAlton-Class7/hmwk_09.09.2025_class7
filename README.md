Date of Class: 09/09/2025

Class 7: EC2 Basics

Task: Build an Amazon Linux EC2 with a bootstrap.

Template: https://github.com/kirkalton-class7/bmc5/blob/main/ec2scrpit

Steps
1. Navigate to EC2 in console.
2. Create NEW EC2 security group. DO NOT USE DEFAULT SG!
3. SG - Inbound Rules
		1. HTTP, Port 80, Source: Anywhere IPv4 (0.0.0.0/0)
		2. SSH, Port 22, Source: Anywhere IPv4 (0.0.0.0/0)
4. DO NOT TOUCH OUTBUND RULES (IF YOU DO, YOU'RE WRONG!)
3. After creating security group click "Launch an instance" then name and tag the instance
4. Select Amazon Linux 2023 AMI
5. Select t2.nano instance type
6. Create and download new keypair
7. In network settings, click "select existing security group" and choose your EC2 security group
8. Navigate to "Advanced Details" and open the drop down menu
9. Copy the plain text (raw) from startup_script.txt and paste it in the "User Data" section.
10. Launch the EC2 instance, then copy the public DNS.
11. Paste the public DNS in a note taking app, then add “http://“ as a prefix to make it a useable link.

Notes:
- Key pair connects a user’s computer to the AWS EC2 via secure shell (SSH).
- Make sure to type http:// before any links are made
    - example: http://ec2-98-84-105-169.compute-1.amazonaws.com
- tags are useful for organizational purpposes, as well as tracking resource usage across the orgnaization, essential for the office!
- ALWAYS TAG RESOURCES!


Tear Down Instructions
1. Click "Instances" on the left hand menu
2. Click the selection box next to your instance.
3. Click the "Instance State" dropdown menu and select "Terminate Instance"
4. Delete the EC2 security group (optional)
