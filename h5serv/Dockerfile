FROM hdfgroup/pytables:3.2.2 
MAINTAINER John Readey <jreadey@hdfgroup.org>
RUN cd /usr/local/src                                    ; \
    git clone https://github.com/HDFGroup/hdf5-json.git  ; \
    cd hdf5-json                                         ; \
    python setup.py install                               

RUN groupadd -r hdfusr && useradd -r -g hdfusr hdfusr    ; \
    mkdir /home/hdfusr && chown hdfusr /home/hdfusr      ; \   
    mkdir /data && chown hdfusr /data                   
    
EXPOSE 5000 5000

USER hdfusr

RUN cd /home/hdfusr                   ; \
    export HOME=/home/hdfusr          ; \
    git clone https://github.com/HDFGroup/h5serv.git  

COPY entrypoint.sh /

ENTRYPOINT ["/entrypoint.sh"]
