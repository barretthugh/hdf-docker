FROM python:3.5
MAINTAINER John Readey <jreadey@hdfgroup.org>
RUN cd /usr/local/src ; \
    mkdir hdf5 ; \
    cd hdf5 ; \
    wget http://www.hdfgroup.org/ftp/HDF5/current/src/hdf5-1.8.16.tar ;\
    tar -xvf hdf5-1.8.16.tar ; \
    cd hdf5-1.8.16 ;\
    ./configure --prefix=/usr/local/hdf5  ; \
    make ; \
    make check ; \
    make install ; \
    make check-install ; \
    for f in /usr/local/hdf5/bin/* ; do ln -s $f /usr/local/bin ; done  
 
