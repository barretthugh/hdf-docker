##  Dockerfile Image for h5serv

## Ingredients:
 
* Python 3.6.2
* hdf5-json package
* h5serv - HDF Rest service

## Instructions

Run with the docker '-d' (for daemon) flag, port mapping, and the data volume to use.

Example:

```$docker run -p 5000:5000 -d -v <mydata>:/data hdfgroup/h5serv:0.1.dev```

Where "mydata" is the path to a folder on the host that (presumably) holds some HDF5
files to be managed by h5serv.

You should then be able to go to http://127.0.0.1:5000 in your browser to view 
data returned by h5serv.

Note: if you are using docker-machine, use: ```docker-machine ip default``` to get the IP
of the virtual machine, and use that IP in place of 127.0.0.1.

## See Also:

See http://h5serv.readthedocs.org/en/latest/ for more information about h5serv.
