FROM hdfgroup/pytables:3.2.2 
MAINTAINER John Readey <jreadey@hdfgroup.org>
RUN mkdir /data                                          ; \
    cd /usr/local/src                                    ; \
    git clone https://github.com/HDFGroup/hdf5-json.git  ; \
    cd hdf5-json                                         ; \
    python setup.py install                              ; \
    cd /usr/local/src                                    ; \
    git clone https://github.com/HDFGroup/h5serv.git     
                              
EXPOSE 5000 5000
  

COPY entrypoint.sh /

ENTRYPOINT ["/entrypoint.sh"]

