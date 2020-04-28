# Docker-CTF
This will help you host a container running a CTF-Capture The Flag event using just one click in just 1 second

This is my project using docker software.
My idea is simple: Launch the CTF events on docker container for smooth management and hastle free server setup.

## GETTING STARTED
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### REQUIREMENTS
1. Any Linux Distro : I have used RHEL8 - REDHAT ENTERPRISE LINUX VERSION 8
2. Any virtualisation tool: I have used Oracle VirtualBox 6.1.4
2. Docker software: I have server version 18.09.1
3. Docker-compose (because it doesn't come pre-installed with docker)

### INSTALLING
1. RHEL8 can be installed as an iso image and then be set up as a new virtual machine using any virtualisation tool like Oracle VirtualBox.
2. Run the following command to install Docker-Community Edition
```
# cd /etc/yum.repos.d/
```
-> now inside this folder create a .repo file and inside it wirte the following:
```
[docker]
baseurl = https://download.docker.com/linux/centos/7/x86_64/stable/
gpgcheck=0
```
-> now run this command to install Docker-Community Edition
```
# yum install docker-ce --nobest
# systemctl enable docker
# systemctl start docker
```
### FINAL STEP
Now just get the yml file into your machine and run the command:
```
# docker-compose up
```
........ and you are good to go!!

Go to your browser, get yourself registered in my database and start your CTF. This is just a prototype and more advance features can be added to it.

### BUILT WITH
* My own precreated docker image 
