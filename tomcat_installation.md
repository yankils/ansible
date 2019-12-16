# Tomcat installation on EC2 instance

### Prerequisites
1. EC2 instance

### Install Apache Tomcat
Install Java 
```sh
   yum install java
```

Download tomcat packages from  https://tomcat.apache.org/download-80.cgi onto /opt on EC2 instance
```sh
  # create tomcat directory
  cd /opt
  wget http://mirrors.fibergrid.in/apache/tomcat/tomcat-8/v8.5.35/bin/apache-tomcat-8.5.35.tar.gz
  tar -xvzf /opt/apache-tomcat-8.5.35.tar.gz
```
give executing permissions to startup.sh and shutdown.sh which are under bin.
```sh
   chmod +x /opt/apache-tomcat-8.5.35/bin/startup.sh shutdown.sh
```
start the tomcat services
```
  cd /opt/apache-tomcat-8.5.35/bin
  ./startup.sh

```
#### check point :
access tomcat application from browser on prot 8080
http://<Public_IP>:8080


