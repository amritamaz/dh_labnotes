## About Clouds
+ AWS - Amazon Web Services
+ imagine what's inside your computer: a motherboard, a hard drive, a networking card, some storage, memory, some other stuff display etc.
+ imagine each part of your computer - each one of those componenets is just a service in the cloud - **you're provisioning a computer**
+ so you can call them up "Hey Amazon! Give me some computer"
+ then you're going to say "hey amazon, I need some hard drive space" - the OS is linux
+ you're going to provision something that's called a block, which is like connecting a hard drive to your computer
+ and then you can connect multiple blocks, and the OS is actually another block attached to your service
+ the computations you provision are a service, the storage is a service
+ the cloud is a collection of services
+ you are effectively buying a computer somewhere, and you are just asking amazon to turn that computer on, to add more hard drives and remote backup etc


### What's the difference between AWS and Dropbox?
+ Underneath the hood, Dropbox looks just like AWS
+ AWS gives you nothing - you have to install your mp3 player and firefox and all of that
+ Dropbox says: get your own computer, and we will just give you some special software to just do the backup ing for you
+ Gmail is a similar ethos: we are a service for just mail, that does backups really really well
+ these services like gmail and dropbox do all the _setup_ for you that you would have done in amazon web services yourself - more configurable, but also more dangerous
+ AWS is your responsibility, dorpbox and gmail asorb a lot of responsibility

### What does the cloud mean?
+ google owns many underground bunkers that just have giant computers
+ gmail underneath is just a bunch of servers and racks somewhere, backing up to "the cloud"
+ it might be that the CPU you use in AWS is in nebraska and one of your storage units is in montana - the cloud is a good metaphor for a distributed space in which all these services as if they are one machine
+ distributed idea

## The Lab
1. Set up an AWS account: aws.amazon.com
2. ONce you're done, click on the cube in the top-left corner to se all of Amazon's Web Services
	- EC2 - we use often
	- Glacier is super cheap and stores multiple copies of everything you own, but wen you want it back it will take 10 minutes
	- S3 - type of storage
	- There are a lot of databases as a service people use
	- IAM - the security feature we are going to use
	- We will spend most of our time in IAM and EC2

+ aside: why is there so much security?
	- companies run, wall street, medical, etc. companies that run on exactly this infrastructure - allowing anyone to hack into their amazon login is absolutely terrible
	- coming into this console from the web is a huge deal

3. Launching an EC2 instance
	- click on EC2, click 'launch instance'
	- what is a server? a server is a computer that serves stuff - you can call it up and say give me some stuff and it will give it to you. this means it's probably connected to the internet - it's set up to give stuff
	- this is how accessing websites works
	- your laptop is not as easily accessible - you can configure your laptop to be a server, you have server software, but if you turn your laptop off, the server goes offline
	- servers tend to be connected and available al the time, and if you are running a company, you have mulitple servers to back the company up, to be avilable for company operations if one breaks down
	- spot requests, reseerved instances - don't wrry about it - ignore this
	- **instance** - an instance is like a virtual server on AWS
	- **images**:
		- on a DVD, they have all these pieces of information, on an application there are all these pieces of information. these are conveyed as an *image*
		- there are different operating systems, and to install things you need an *image* of that running
		- think of it like DVDs - dvds have images
		- turns out there are hundreds of them, and there are special images for special servers taht do things - these special servers are called AMIs, and we're going to use these images
	- **elastic blocks** - in the physical world they are equivalent to hard drives or volumes
	- **snapshots** - if you have a block, you can take a snpashot of it, which is like a backup - snapshots automatically go to glacier, cheap storage, so it's a way to save a version of the data as it stands right now
	- click a button called 'Launch an Instance'
	- then it asks, choose an image - which dvd do you want to put in
	- bc dennis uses a Debian-64 environment, we are going to use Debian-64
		- go to the AWS Marketplace, search for debian
		- **make sure it is FREE TIER ELIGIBLE** - should be labelled under the image
		- select the Debian 64-bit one
		- **make sure you select the t1.micro machine** - this is the free one
		- from amazon: "Micro instances are eligible for the AWS free usage tier. For the first 12 months following your AWS sign-up date, you get up to 750 hours of micro instances each month. When your free usage tier expires or if your usage exceeds the free tier restrictions, you pay standard, pay-as-you-go service rates."
		- click 'next: configure instance details'
		- we are going to only run one instance
		- shutdown behavior: leave at "stop"
		- protect from accidental termination? yes sounds good (check this off)
		- enable cloudwatch? no, we don't care about traffic and analytics
		- next: add storage
		- hit next: tag instance
		- leave key as "Name" and make value something like "myfirstserver"
		- hit next, but we are NOT going to change
		- click review and launch
		- click Launch!
		- KEY PAIRS GET READY
			- Create a new key pair
			- Name it whatever "myfirstkey"
			- Click DOWNLOAD KEY PAIR
			- save it somewhere safe
			- then launch instance
		- see how it says "view Usage Instructions"? Click on it
			- this computer is new and vanilla and it has nothing on it
			- when you turn it on, you don't have a login, so how do you login?
			- in the real world they make a fake user for you or ask you to create an account. we don't get those niceities, instead we must use ssh
			- REMEMBER WHAT THE PAGE SAYS: "You must use an SSH client to access this instance, authenticating with your SSH key as the user 'admin'; you may then use 'sudo -i' to gain root (administrator) privileges."
		- now you can click on the cube in the top corner so you're done and go back to EC2
		- Now it should say 1 running instance, 1 volume, 1 key pair, etc
		- if you click on '1 running instance' it should say your computer name
		- this server can run 24/7 for **one year, for free** - after that, you pay for what you use - when the server ison, **you pay per hour**
		- if you're only using it for research or a project, you may want to get in the habit of stopping your instance every time you are done
		- **how to stop your server**: right click on the server name in the instances page, and say *stop*
