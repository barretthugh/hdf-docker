##  Dockerfile Image for HDF5 library with Python 3

## Ingredients:
 
* Python 3.6.2
* HDF5 Library
* HDF5 Tools (h5dump, h5ls, h5repack, etc.)

## Instructions

Launch the container interactively. 

Example:

```$docker run -it -v <mydata>:/data hdfgroup/hdf5lib:1.8.16 /bin/bash```

Where "mydata" is the path to a folder on the host that (presumably) holds some HDF5
files.  

From the bash prompt you should then be able to use tools such as h5dump or h5repack on
the mounted data files.

## See Also:
Checkout https://www.hdfgroup.org/HDF5 for information on how to use HDF5.
