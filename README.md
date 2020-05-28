# docker_project
This is my docker project to host a ghost webapp. I have used MYSQL in the back-end and ghost server in the front-end.

About Ghost -
Ghost is a free and open source blogging platform written in JavaScript and distributed under the MIT License, designed to simplify the process of online publishing for individual bloggers as well as online publications.

Requirement :-
You will require an O.S. to host this webapp (I have used RHEL8).
yum should be configured.
Process :-
1.Docker Installation :-
To install docker , run this command on terminal yum install docker-ce --nobest
2.Run the Docker :-
To start the docker we will use this command systemctl start docker
3.Download the required Images :-
command to download mysql version 5.7 image => docker pull mysql:5.7
command to download ghost version 1-alpine image => docker pull ghost:1-alpine
4.Now setup the MYSQL server :-
To setup MQSQL use docker run -dit -e MYSQL_ROOT_PASSWORD=# Enter a password # -e MYSQL_USER=# Enter a username # -e MYSQL_PASSWORD=# Enter a password other than root password # -e MYSQL_DATABASE=#Enter a database name # --name # Enter a name # mysql:5.6
5.Docker-compose installation and creation docker-compose file :-
commands to install docker-compose :-
curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
after installation create a folder using mkdir mycompose command
In that folder create your docker-compose file using vim docker-compose.yml
6.To start the server :-
run this command in the folder where docker-compose file has been created docker-compose up
7.To stop the server :-
to stop the server run this command in same folder where you have created your compose file docker-compose down 
8. To access the webapp :-
start the server and go to you browser and search http://localhost:2368/ or `http://192.168..x.x:8081
