<p align="center">
<img src="https://i.imgur.com/hWjHdkl.png" height="25%" width="25%"/>
</p>
<h1>Launching and Connecting to an EC2 Instance in AWS</h1>
In this project, I launched an EC2 instance and connected to the instance using an SSH client. Instances are virtual servers that launch into a VPC subnet and consist of 4 components: CPU, memory, disk, and networking. Also, since instances launch into VPC subnets and subnets are AZ resilient, EC2 instances are also AZ resilient.
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
Now that the key pair is created, it's time to create an instance. I went back to the EC2 Dashboard and clicked on "Instances" under "Instances." For the AMI (Amazon Machine Image) for the instance - which is the version of the operating system that the instance will run, - I went with the default of Amazon Linux. Under "Key pair (login)," I selected the key pair I created in the previous step. Lastly, under "Network settings" I created a security group, which essentially acts as a mini firewall, and then launched the instance. Although this is my first time using Security Groups in AWS, I used a Security Group in Azure to create an inbound security rule denying ICMP traffic; if you're curious about that, check out my Wireshark project!
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/caVfsxz.png" height="80%" width="80%"/>
</p>
<p>
The instance might take a few minutes to set up, so be prepared to wait for a little during this part. The "Instance state" will start as "Pending" and eventually transition to "Running." At this point, the "Status check" will be "Initializing" and will eventually say "2/2 checks passed." Clicking the Refresh button at the top of the screen next to the "Connect" button will help with knowing where you are in the process. Once that's done, I connected to the instance by right-clicking on it and selecting "Connect."
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/1bLZss7.png" height="80%" width="80%"/>
</p>
<p>
As you can see, there are a few ways to connect to an instance. Using EC2 Instance Connect connects you to the instance using a web console, which means that through your web browser, you'll be taken to the terminal of the EC2 instance and automatically connect. However, I created an SSH key pair earlier in the lab that I wanted to use to connect to my instance, so I connected using an SSH client.
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/vSzOdee.png" height="80%" width="80%"/>
</p>
<p>
To begin the process of connecting to the instance using SSH, I opened up the Windows CLI. Since I downloaded my part of the SSH key pair to my Downloads folder, I used the "cd" command to move to my Downloads folder. On the "Connect to instance" page, I copied and pasted the command under "Example:" into the CLI; this command uses the local SSH client and the downloaded key to connect to the EC2 user and instance. After running the command and confirming that I wanted to continue connecting, I was now connected to my EC2 instance!
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/ix293LH.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/0oQmOOt.png" height="80%" width="80%"/>
</p>
<p>
Last but not least: clean up. Although I stayed in the Free Tier for this lab, it's good practice to delete what you no longer need in order to avoid clutter and unnecessary charges. I first terminated the instance by right-clicking on it and selecting "Terminate instance." Next, I went to "Network & Security" -> "Security Groups" and selected the security group I created with the instance, and then selected "Actions" -> "Delete security groups." 
</p>
<br />
<br />

<p>
✨ This was my first time using AWS aside from creating accounts or configuring billing and security settings, and I have to say, it was pretty fun! While connecting to an instance with EC2 Instance Connect seems easier, I'm glad I learned how to connect using the CLI. I'm still pretty early in my AWS journey, but I'm excited to learn more and work towards completing complex projects.
</p>
<br />
