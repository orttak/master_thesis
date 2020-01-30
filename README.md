# Master Thesis

## Install Docker
For installing Docker, you can follow the official document. 
##### Windows Users
[1- Enabled virtualization ](https://docs.docker.com/docker-for-windows/troubleshoot/#virtualization-must-be-enabled)

[2-You can download Docker Desktop for Windows from Docker Hub.](https://docs.docker.com/docker-for-windows/install/)

## Download Application 
There are two ways to download the application. You can direct download .zip file, extract the zip file to working directory and open CMD in working directory and continue with Running Docker section. The second way to download the data using Git. Open CMD and follow the below steps.
```
cd working_directory
```
```
git clone https://github.com/orttak/master_thesis.git
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
docker exec -it   containerID  /bin/bash
```
You can learn containerID with 'docker ps' command.

## DESIGN OF THE AUTOMATED WEB BASED DATA ANALYSIS SYSTEM COMPONENTS

In recent years with the improvements in data resolution and data collection methods, a new era called ‘Big Data’ has started. As the amount of data increases, it also brings new needs to increase in storage and the technical needs to analyse the data. However, cloud computing has a beneficial structure for the users in terms of high storage space, powerful machines, wideband substructure, splitting the sources depending on needs, pay as you go policy and the low cost starting investments.

With the help of virtualization, we can create individual machines using the qualifications the system already has, such as processor, storage and so on. Those machines can work on one application for its different elements focusing on different tasks, or it can work for completely different applications. The solutions that are offered by visualization technologies have been changing throughout the years. For example, the Docker system has been developed, as an alternative to the virtual machines since the virtual machines have been using more sources of the system. The docker system has become more and more famous because of its efficiency on using the system sources, as well as the speed it has been offering.

The docker technology did not just offer a new experience for cloud computing but also for personal computer usage as well. Many applications and code databases have been served to the users without any problem with the help of this system. While the set up of some applications, it is very likely to face some problems in the communication between dependent structures and to keep some applications working properly. The developers are aiming the users to face a minimum amount of problems, by putting all the proper and needed substructures into one package and serve a more stable application, with the help of docker. The Docker file which was created in the application section is an example of the usage of this structure. 
Remote sensing systems have also been affected by the rapid improvement in the data systems. The investments and the free data by ESA, the data substructure by USGS and the investments on the satellite technologies by private companies have improved the remote sensing data quality, diversity and capacity. One of the main purposes of those associations is to provide the data to more and more users. With this aim, all the resources of cloud computing systems have been used together with the remote sensing data.

New remote sensing applications have been developed recently using the skills of cloud computing, such as creating an environment to use in remote sensing data analysis, to begin with. The big data providing companies such as Digital Globe, Airbus, Planet have created an environment that allows the users to reach the data faster and perform analyses on the cloud computing substructure. The user can fulfil all the needs with only one service, and in a fast way. In the thesis master thesis work, it has been investigated how user requests work in the background of GBDX service by Digital Globe company. The role of the Docker system in such a structure has been explained. 
The second type of application is the services that come out from the changes while publishing the remote sensing data. We can also define them as systems that are faster and easier compared to the old traditional methods while reaching the data. With the help of the API services offered by data producers, the users can discover the target image faster by data searching tools using different programming languages. It also gives the user the chance to reach only the needed bands for a specific topic, by publishing the satellite image bands separately instead of serving it in a compressed format altogether. This method increases the speed of reaching the data, as well as it allows developing different applications using programming languages such as Python or JavaScript.

In this master thesis, a remote sensing application has been carried out with the help of Python programming language, using the Landsat-8 data providing application programming interface (API) which is created with the collaboration of USGS, Planet and Amazon companies. With the big data era, API services are more important to find and download the data. Many companies create process service for user, also they create API services to increase user experience. GBDX is good example for new generation application. In this Master thesis, explain process service but also, user can find and process data with GBDX API in their local environment.

Python programming language provides different solutions to different users, particularly in web-based applications, data analysis, machine learning, and deep learning, also in many others. The main part of this open-source developing language based on the libraries that were developed for applications. Python libraries are known to be very rich in terms of geographical libraries including the satellite data.

For the analyses that are carried out with cloud computing, there is a need to have an interface between the system and the user. To cover this need, the Jupyter application has been created. With the help of Jupyter, it is possible to do analyses, visualization of the results and to save the outcomes in our device or a personal computer on the cloud system, using a web browser.

A remote sensing application has been designed using Landsat-8 API on Jupyter notebooks. This application includes every step of a remote sensing application, from the collection of the data till the producing of the data. In the first step, the target images have been detected depending on the image ID or the working area. A structure has been created where technical details can be included as search criteria, such as the date and the cloud percentage.In this step, according the scope of application, people change their searching algorithm. For small applicaiton, user define images on Glovis that USGS search engine system and collect the data ID and download the image with targeting bands. Also,  After the detection and the download of the convenient bands according to the aim of the work, Jupyter files have been created to complete the following actions respectively: data preprocessing, creating a true-color image combination, create indices (e.g. NDVI), clipping of the image according to the working is and the classifications.
newpage

The Docker file has been created to use the generated Jupyter files. This file allows the users to create a similar substructure with every operating system and cloud. They will also be able to support and improve the system with the Git version control system, using the errors they get and the improvements they make. Github is the most popular service that has Git version control system. Users can reach Docker file on Github and download the Docker system to create services. If the user get an error while using a script or developing a new algorithm with Git ability, they can send the error or the new Jupyter file to the Github project and the system fixes the errors and improve the application area.

Since the Docker file and the Jupyter files it includes have a structure that is open for improvement, a similar structure can be added to the system for different satellite images or the Jupyter files of different applications that have been made with Landsat-8 images. Also, a similar system can be served to users as a service in a cloud computing environment.
