# hdf-docker

This repository conatins Dockerfiles for various HDF-related containers.
Dockerfiles for HDF related containers.

## Installation
The containers were built using Docker 1.10.x.  
Go to https://www.docker.com to install docker.

## Building and running containers

To build a container, cd to one of the folders in this repository, and run:

```$ docker build -t PATH .```

To launch a container, run:


```$ docker run -t PATH /bin/bash```

See the Docker documentaion for information on the different docker commands that you can use.

## Docker hub

Images of all the containers listed here are available on Docker Hub: https://hub.docker.com.

For example, running:


```$ docker pull hdfgroup/hdf5/lib:1.8.16```

will launch the container with the 1.8.16 release of the HDF5 library.
