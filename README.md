myTomcatDocker
======================
Quick environment for developing Web applications.

Author: Ming Zhao mingyu.zhao@gmail.com

Requirements
------------
Docker

Configuration
---------------
In “config.json”, you can set the port and endpoints of API services, as well as WSO2 IS params.

Installation
------------
docker build -t my-tomcat-8.5 . 

docker run -it --rm --name my-running-tomcat -p 8080:8080 -v $PWD/webapps:/usr/local/tomcat/webapps -v $PWD/conf:/usr/local/tomcat/conf my-tomcat-8.5


Testing
-----------
Given:

Container IP: 192.168.99.100 

Then go to:

http://192.168.99.100:8080


Resources
---------
* [Docker](http://www.docker.com)


