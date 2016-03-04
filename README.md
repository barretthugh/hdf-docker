# hdf-docker

This repository contains Dockerfiles for various HDF-related containers.

Dockerfiles are text files that contain the instructions for building a Docker image. 

## Installation
The containers were all built using Docker 1.10.x.  
Go to https://www.docker.com for information on how to install docker.

## Building and running containers

To build a container, cd to one of the folders in this repository, and run:

```$ docker build -t PATH .```

To launch a container, run:


```$ docker run -it PATH /bin/bash```

See the Docker documentaion for information on the different docker commands that you can use.

## Docker hub

Images of all the containers listed here are available on Docker Hub: https://hub.docker.com.

For example, running:


```$ docker pull hdfgroup/hdf5lib:1.8.16```

will retrieve the container with the 1.8.16 release of the HDF5 library.

Or you can simply run:

```$ docker run -it hdfgroup/hdf5lib:1.8.16 /bin/bash```

And the image will be downloaded from Docker Hub if it is not already present on your machine
and then run.
