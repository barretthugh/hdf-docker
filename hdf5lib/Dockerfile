FROM python:3.5
MAINTAINER John Readey <jreadey@hdfgroup.org>
RUN cd /tmp                                                                        ; \
    wget http://www.hdfgroup.org/ftp/HDF5/releases/hdf5-1.8.16/src/hdf5-1.8.16.tar ;\
    tar -xvf hdf5-1.8.16.tar --directory /usr/local/src                            ; \
    rm hdf5-1.8.16.tar                                                             ; \
    cd /usr/local/src/hdf5-1.8.16                                                  ; \
    ./configure --prefix=/usr/local/hdf5                                           ; \
    make                                                                           ; \
    make check                                                                     ; \
    make install                                                                   ; \
    make check-install                                                             ; \
    for f in /usr/local/hdf5/bin/* ; do ln -s $f /usr/local/bin ; done             ; \
    pip install numpy                                                              ; \  
    cd /usr/local/src                                                              ; \
    git clone https://github.com/h5py/h5py.git                                     ; \
    cd h5py                                                                        ; \
    export HDF5_DIR=/usr/local/hdf5                                                ; \
    python setup.py build                                                          ; \
    python setup.py install           
 
