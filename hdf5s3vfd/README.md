##  Dockerfile Image for HDF5 library with S3 VFD

## Ingredients:
 
* CentOS
* HDF5 Library
* h5py

## Introduction

The S3VFD is a virtual file driver with support for reading from HDF5 files 
stored as S3 objects.

## Instructions

Launch the container interactively. 

Example:

```$docker run -it -v ${HOME}:/home hfgroup/hdf5s3vfd /bin/bash
   # export PATH=/usr/local/src/s3vfd/bin/:$PATH
   # h5dump -f ros3 http://s3.amazonaws.com/hdfgroup/data/hdf5demo/tall.h5 ```

From the bash prompt you should then be build any HDF5 program for which you have
source in your home directory.

 

 