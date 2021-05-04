# Uesrs :

Create a user for running the application.

```
#apt update
#useradd -m -s /bin/bash todoapp
#cd /home/todoapp/
```
Lets clone the code from github repository.

```
# git clone https://github.com/zelar-soft-todoapp/users.git
```
Shipping service is written in Java, Hence we need to install Java.

Update and Install Maven, This will install Java too.

```
# apt update
# apt install openjdk-8-jre-headless
# apt install openjdk-8-jdk-headless
# export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
# apt install maven -y
# cd /home/todoapp/users/
# mvn clean package  
# cd target/
```
Note : User Component will be running with port : 8080

Finally start the Uesrs Module once to effect the changes by the below cammand.
```
# java -jar users.jar
```
