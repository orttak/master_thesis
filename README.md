# Master Thesis

## Install Docker
For installing Docker, you can follow the official document. 
##### Windows Users
[1- Enabled virtualization ](https://docs.docker.com/docker-for-windows/troubleshoot/#virtualization-must-be-enabled)
[2-You can download Docker Desktop for Windows from Docker Hub.](https://docs.docker.com/docker-for-windows/install/)

##Download Application 
There are two ways to download the application. You can direct download .zip file, extract the zip file to working directory and open CMD in working directory and continue with Running Docker section. The second way to download the data using Git. Open CMD and follow the below steps.
```
cd working_directory
```
```
git clone git@github.com:orttak/master_thesis.git
```

```
cd master_thesis
```

## Running Docker


```
cp default.env .env
```
Create Docker service
```
docker-compose up -d --build
```
After creating service you can check the Docker service with ' docker ps ' on CMD.
Go to  http://127.0.0.1:9999/lab 


Open Docker container command 
```
docker exec -it   containerID
```
You can learn containerID with 'docker ps' command.


