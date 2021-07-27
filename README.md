# Uesrs :

Create a user for running the application.

```
# apt update
# useradd -m -s /bin/bash todoapp
# cd /home/todoapp/
```
Lets clone the code from github repository.

```
# git clone https://github.com/zs-amrutha/users.git
```
Shipping service is written in Java, Hence we need to install Java.

Update and Install Maven, This will install Java too.

```
# apt update
# apt install openjdk-8-jre-headless -y
# export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
# apt install maven -y
# cd /home/todoapp/users/
# mvn clean package  
# mv target/users-api-0.0.1.jar users.jar
```
Note : User Component will be running with port : 8080

Finally start the Uesrs Module once to effect the changes by the below cammand.

```
# mv /home/todoapp/users/systemd.service /etc/systemd/system/users.service
# systemctl daemon-reload && systemctl start users && systemctl enable users 

```
;) ;)
# RELEASE 0.0.1 -DATE - 03-06-2021
# RELEASE 0.0.2 -DATE - 09-06-2021
# RELEASE 0.0.3 -DATE - 12-06-2021
