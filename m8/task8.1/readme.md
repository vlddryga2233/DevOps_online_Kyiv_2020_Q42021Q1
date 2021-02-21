# Task 8.1
1. Create 2 instance in AWS


> First instance it is a Jenkins server

> Second instance it is a web server on wich will be our application

<img src="./screenshot/aws_instance.png" >

2. Install java on each instance 

```
sudo apt-get install openjdk-8-jdk
```

3. Install .net core and nginx server

```
wget https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb

sudo apt-get update; \
  sudo apt-get install -y apt-transport-https && \
  sudo apt-get update && \
  sudo apt-get install -y dotnet-sdk-5.0

  sudo apt-get update; \
  sudo apt-get install -y apt-transport-https && \
  sudo apt-get update && \
  sudo apt-get install -y aspnetcore-runtime-5.0

  sudo apt-get nginx
```

4. Configure webserver

> Setup nginx as reverse-proxy server 

<img src="./screenshot/nginx_config.png" width="50%">

> Setup service that will be launch .net app

<img src="./screenshot/dotnet_service.png" width="50%">

5. Create app in Visual Studio

> Create Asp .Net Core app based on MVC pattern

6. Push app on github

    <img src="./screenshot/github_repos.png" width="50%">

7. User Jenkins to build app on the webserver

> Create node and determine connection
<img src="./screenshot/web-server_slave.png" width="90%">

> Create job

> Connect to repos by jenkins
<img src="./screenshot/job_repos.png" width="80%">

> Determine commands to build app on the server
<img src="./screenshot/job_script.png" width="1000%">


> Start job and get console output
<img src="./screenshot/console_output.png" width="90%">

> Check changes on the server
<img src="./screenshot/web-site.png" width="90%">

8. Change womething in the project



<img src="./screenshot/project_changes2.png" width="70%">



9. Start job to build new version

<img src="./screenshot/second_build.png">

<img src="./screenshot/get_changes.png" width="90%">
