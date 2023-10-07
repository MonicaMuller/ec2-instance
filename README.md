<p align="center">
<img src="https://i.imgur.com/hWjHdkl.png" height="25%" width="25%"/>
</p>
<h1>Launching and Connecting to an EC2 Instance in AWS</h1>
In this project, I launched an EC2 instance and connected to the instance using an SSH client. Instances are virtual machines/servers that launch into a VPC subnet and consist of 4 components: CPU, memory, disk, and networking. Also, since instances launch into VPC subnets and subnets are AZ resilient, EC2 instances are also AZ resilient.
<br />
<br />

<h2>Technologies Used</h2>

- Amazon Web Services (AWS)
- Elastic Cloud Compute (EC2)
- Windows CLI
- SSH
- Key pairs
- Security Groups
<br />

<h2>High-Level Steps</h2>

- Log into AWS and go to the EC2 Dashboard
- Create an SSH key pair
- Create and then launch an EC2 instance
- Connect to the instance using an SSH client
- Terminate the instance and corresponding security group
<br />

<h2>Synopsis</h2>

<p>
<img src="https://i.imgur.com/dawUj0D.png" height="80%" width="80%"/>
</p>
<p>
I used an IAM user in my general training account for this lab and stayed in the AWS Free Tier. Once I was logged in, I made my way to the EC2 Dashboard by typing "ec2" in the Search bar at the top.
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/t2IWflU.png" height="80%" width="80%"/>
</p>
<p>
After arriving at the EC2 Dashboard, I scrolled down the options on the left side of the screen and selected "Key Pairs" under "Network & Security." Key pairs consist of 2 parts, one which AWS keeps and the other which the user downloads. Since modern versions of Windows come with a version of SSH and I am using a modern version of Windows, I selected ".pem" for the "Private key file format." I then clicked on "Create key pair" and downloaded the private part of the key pair (this is the only chance to download your part of the key pair, otherwise you'd need to create another key pair).
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/sBiOMII.png" height="80%" width="80%"/>
</p>
<p>
Lorem ipsum
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/LVL3xjV.png" height="80%" width="80%"/>
</p>
<p>
Lorem ipsum
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/1bLZss7.png" height="80%" width="80%"/>
</p>
<p>
Lorem ipsum
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/vSzOdee.png" height="80%" width="80%"/>
</p>
<p>
Lorem ipsum
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/ix293LH.png" height="80%" width="80%"/>
</p>
<p>
Lorem ipsum
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/0oQmOOt.png" height="80%" width="80%"/>
</p>
<p>
Lorem ipsum
</p>
<br />
<br />

<p>
✨ Lorem ipsum
</p>
<br />
