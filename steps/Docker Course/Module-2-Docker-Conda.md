# Docker Ancaconda (Docker) Course - Module 2
This is my Docker course. I hope you like it.

> These notes follow on from the README.md getting started instructions.
***
***

## Docker Conda                                          Docker تشغيل أناكوندا بداخل   ##
To download Docker with anaconda image               حمل صورة لنظام دوكر يشمل أناكوندا 

>Steps/Commands
You should now have a directory called 'drf_course' in your development directory. This will be known as your 'root directory'.


Docker is an open platform for developers and system administrators to build, ship, and run distributed applications, whether on laptops, data center virtual machines, or the cloud. Anaconda, Inc. provides Anaconda and Miniconda Docker images.

>Read the official Docker documentation and specifically the information related to Docker Conda image and installation.

```
https://docs.anaconda.com/free/anaconda/applications/docker/
```
Begin by browsing the available Anaconda images on our Docker profile.

To obtain a fully working Anaconda image:

In a terminal window, run this command to display a list of available images:

docker search continuumio
Pull the desired image:
```
docker pull continuumio/miniconda3
```
Create a container using the image:
```
docker run -t -i continuumio/miniconda3 /bin/bash
```
This gives you direct access to the container where the conda tool is already available.

Test the container:

```
conda info
```
You now have a fully working Anaconda image.

