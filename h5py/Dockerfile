FROM hdfgroup/hdf5lib:1.8.16
MAINTAINER John Readey <jreadey@hdfgroup.org>
RUN    pip install numpy                 ; \  
       cd /usr/local/src                 ; \
       git clone https://github.com/h5py/h5py.git ; \
       cd h5py                           ; \
       export HDF5_DIR=/usr/local/hdf5   ; \
       python setup.py build             ; \
       python setup.py install           
      
      

