FROM centos
MAINTAINER John Readey <jreadey@hdfgroup.org>                                            
ENV HDF5_SRC_URL  https://bitbucket.hdfgroup.org/scm/hdffv/hdf5.git    
ENV HDF5_INSTALL_DIR /usr/local/src/s3vfd/build           
RUN yum -y install gcc gcc-c++                                                        ; \
    yum -y install git                                                                ; \                                       
    yum -y install make                                                               ; \
    yum -y install which                                                              ; \
    yum -y install autofconf                                                          ; \
    yum -y install libtool                                                            ; \
    yum -y install curl-devel                                                         ; \
    yum -y install openssl-devel                                                      ; \
    cd /usr/local/src                                                                 ; \
    git clone ${HDF5_SRC_URL} s3vfd                                                   ; \
    cd s3vfd                                                                          ; \
    git checkout RO_S3_VFD                                                            ; \
    ./autogen.sh                                                                      ; \ 
    RV_OPTS="${RV_OPTS} --with-hdf5=${HDF5_INSTALL_DIR}"                              ; \
    COMP_OPTS="-Wall -pedantic -Wunused-macros"                                       ; \       
    ./configure --prefix=${INSTALL_DIR} ${RV_OPTS} CFLAGS="${COMP_OPTS}"              
#    make  && make install || exit 1                        
     
     