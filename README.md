# Docker-CTF
This will help you host a container running a CTF-Capture The Flag event using just one click in just 1 second

This is my project using docker software.
My idea is simple: Launch the CTF events on docker container for smooth management and hastle free server setup.

## GETTING STARTED
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### REQUIREMENTS
* Any Linux Distro : I have used RHEL8 - REDHAT ENTERPRISE LINUX VERSION 8
* Any virtualisation tool: I have used Oracle VirtualBox 6.1.4
* Docker software: I have server version 18.09.1
* Docker-compose (because it doesn't come pre-installed with docker)

### INSTALLING
* RHEL8 can be installed as an ISO image and then be set up as a new virtual machine using any virtualisation tool like Oracle VirtualBox.
* Run the following command to install Docker-Community Edition
```
# cd /etc/yum.repos.d/
```
-> now inside this folder create a .repo file and inside it write the following:
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
-> now follow the steps to download docker-compose
```
# curl -L "https://github.com/docker/compose/releases/download/1.23.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
# chmod +x /usr/local/bin/docker-compose
```
### FINAL STEP
Now just get the docker-compose.yml file into your local machine and run the command:
```
# docker-compose up
```
And you are good to go!!

Go to your browser, get yourself registered in my database and start your CTF. This is just a prototype and more advance features can be added to it.

### BUILT WITH
* My own precreated docker image:
  * has a client side mysql
  * has php and major dependencies -> php-common, php-mysql, php-pdo, php-soap, php-xml, php-mysqlnd
  * net-tools for basic features like netstat for port numbers and ifconfig for IP
  * httpd for hosting apache web server
* Another image of mysql:5.7 to store the data in the databse.

### FEATURES
* The storage where the web pages are loaded and the database is stored is Persistant and not Ephemeral.
* This means that any container if gets corrupted by chance, THE DATA IS NEVER LOST.
* Simply just attach the volume to a new container.
* This Container provides you the luxury to host a docker container with just 1 click and also terminate and wipe off everything without even loosing the data.

### SCOPE OF IMPROVEMENT
* Right now the IP Address in the php file is hardcoded. 
* I have to change that to a dynamic one, so that whenever a new IP is alloted to the sql server the webpage gets connected to it easily.
* More advance CTF will be soon added, right now this is just a PROTOTYPE.
