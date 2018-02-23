##  Dockerfile Image for HDF5 library with HDF REST VOL

## Ingredients:
 
* CentOS
* HDF5 Library
* HDF5 REST VOL

## Introduction

The REST VOL plugin is a plugin for HDF5 designed with the goal of allowing
HDF5 applications, both existing and future, to utilize web-based storage
systems by translating HDF5 API calls into HTTP-based REST calls, as defined
by the HDF5 REST API (see section IV for more information on RESTful HDF5).

Using a VOL plugin allows an existing HDF5 application to interface with
different storage systems with minimal changes necessary.The plugin
accomplishes this by utilizing the HDF5 Virtual Object Layer in order to
re-route HDF5's public API calls to specific callbacks in the plugin which
handle all of the usual HDF5 operations. The HDF5 Virtual Object Layer is an
abstraction layer that sits directly between HDF5's public API calls and the
underlying storage system. In this manner of operation, the mental data
model of an HDF5 application can be preserved and mapped onto storage
systems that differ from a native filesystem, such as Amazon's S3.

## Instructions

Launch the container interactively. 

Example:

```$docker run -it -v ${HOME}:/home hfgroup/restvol /bin/bash```


From the bash prompt you should then be build any HDF5 program for which you have
source in your home directory once you have added the function call to initialize the plugin:
RVinit().  See: https://bitbucket.hdfgroup.org/users/jhenderson/repos/rest-vol/browse/README.txt 
for detailed instructions on building and applications with the REST VOL.

To run the application, you will need to define the following environment variables:

  * HSDS_ENDPOINT: The url endpoint of the HSDS server
  * HSDS_USERNAME: The HSDS account username
  * HSDS_PASSWORD: The HSDS account password

The HSDS adminstrator can provide these settings for you.

 