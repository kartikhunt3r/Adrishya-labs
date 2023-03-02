# Adrishya-labs
easy to install script for pentest labs. 

Bash script to manage web apps using docker and hosts aliases.  
Made for Kali linux, but should work fine with pretty much any linux distro.

### Current available webapps

* bWAPP
* WebGoat 7.1
* WebGoat 8.0
* Damn Vulnerable Web App
* Mutillidae II
* OWASP Juice Shop
* WPScan Vulnerable Wordpress
* OpenDNS Security Ninjas
* Altoro Mutual
* Vulnerable GraphQL API


## Installation: 

Using any of these apps can be done in 3 quick and simple steps.

#### 1) Clone the repo
Clone this repo, or download it any way you prefer
```
git clone https://github.com/kartikhunt3r/Adrishya-labs.git
cd Adrishya-labs
```

#### 2) Install docker
```
sudo apt install docker.io
```

## Use:

#### 1) Start an app on localhost
Now you can start and stop one or more of these apps on your system.
As an example, to start bWAPP just run this command
```
./adrishya_labs.sh start bwapp
```
This will download the docker, add bwapp to hosts file and run the docker
mapped to one of the localhost IPs.
That means you can just point your browser to http://bwapp and it will be up
and running.


#### 2) Start an app and expose it from machine
Use the startpublic command to bind the app to your IP
```
./adrishya_labs.sh startpublic bwapp
```
If you have multiple interfaces and/or IPs, **or** you need to expose the app on a different port specify it like this
```
./adrishya_labs.sh startpublic bwapp 192.168.1.105 8080
```
IP needs to be an IP on the machine and port in this example is 8080

You can only have one app exposed on any given port. If you need to expose more than one app, you need to use different ports.


#### 3) Stop any app
To stop any app use the stop command
```
./adrishya_labs.sh stop bwapp
```


#### Print a complete list of available projects use the list command
```
./adrishya_labs.sh list 
```

#### Running just the script will print help info
```
./adrishya_labs.sh 
```


## Help
```
Usage: ./adrishya_labs.sh {list|status|info|start|startpublic|stop} [projectname]

 This scripts uses docker and hosts alias to make web apps available on localhost"

Ex.
./adrishya_labs.sh list
   List all available projects  

./adrishya_labs.sh status
   Show status for all projects  

./adrishya_labs.sh start bwapp
   Start docker container with bwapp and make it available on localhost  

./adrishya_labs.sh startpublic bwapp
   Start docker container with bwapp and make it available on machine IP 

./adrishya_labs.sh stop bwapp
   Stop docker container

./adrishya_labs.sh info bwapp
   Show information about bwapp project
```


## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://kartiksavaliya.tech/)

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://in.linkedin.com/in/kartikhunt3r)

[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/kartikhunt3r)

[![youtube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/channel/UCqUKMBA2UPqKOYbSa9FnC-Q)

