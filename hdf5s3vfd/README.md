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
   # export PATH=/usr/local/src/s3vfd/build/bin/:$PATH
   # h5dump -f ros3 http://s3.amazonaws.com/hdfgroup/data/hdf5demo/tall.h5 
```

From the bash prompt you should then be build any HDF5 program for which you have
source in your home directory.

## Notes

Running the h5py test suite gives an error:

```
   # cd /usr/local/src/h5py
   # pip install pytest
   # python setup.py develop
   # pytest -v
==================================================================== test session starts ====================================================================
platform linux2 -- Python 2.7.5, pytest-3.4.1, py-1.5.2, pluggy-0.6.0 -- /usr/bin/python
cachedir: .pytest_cache
rootdir: /usr/local/src/h5py, inifile:
collected 455 items

h5py/tests/hl/test_attribute_create.py::TestArray::test_int PASSED                                                                                    [  0%]
h5py/tests/hl/test_attribute_create.py::TestArray::test_string_dtype PASSED                                                                           [  0%]
h5py/tests/hl/test_dataset_getitem.py::TestEmpty::test_ellipsis PASSED                                                                                [  0%]
h5py/tests/hl/test_dataset_getitem.py::TestEmpty::test_fieldnames PASSED                                                                              [  0%]
h5py/tests/hl/test_dataset_getitem.py::TestEmpty::test_index PASSED                                                                                   [  1%]
h5py/tests/hl/test_dataset_getitem.py::TestEmpty::test_indexlist PASSED                                                                               [  1%]
h5py/tests/hl/test_dataset_getitem.py::TestEmpty::test_mask PASSED                                                                                    [  1%]
h5py/tests/hl/test_dataset_getitem.py::TestEmpty::test_ndim PASSED                                                                                    [  1%]
h5py/tests/hl/test_dataset_getitem.py::TestEmpty::test_shape PASSED                                                                                   [  1%]
h5py/tests/hl/test_dataset_getitem.py::TestEmpty::test_slice PASSED                                                                                   [  2%]
h5py/tests/hl/test_dataset_getitem.py::TestEmpty::test_tuple PASSED                                                                                   [  2%]
h5py/tests/hl/test_dataset_getitem.py::TestScalarFloat::test_ellipsis PASSED                                                                          [  2%]
h5py/tests/hl/test_dataset_getitem.py::TestScalarFloat::test_fieldnames PASSED                                                                        [  2%]
h5py/tests/hl/test_dataset_getitem.py::TestScalarFloat::test_index PASSED                                                                             [  3%]
h5py/tests/hl/test_dataset_getitem.py::TestScalarFloat::test_indexlist PASSED                                                                         [  3%]
h5py/tests/hl/test_dataset_getitem.py::TestScalarFloat::test_mask PASSED                                                                              [  3%]
h5py/tests/hl/test_dataset_getitem.py::TestScalarFloat::test_ndim PASSED                                                                              [  3%]
h5py/tests/hl/test_dataset_getitem.py::TestScalarFloat::test_shape PASSED                                                                             [  3%]
h5py/tests/hl/test_dataset_getitem.py::TestScalarFloat::test_slice PASSED                                                                             [  4%]
h5py/tests/hl/test_dataset_getitem.py::TestScalarFloat::test_tuple PASSED                                                                             [  4%]
h5py/tests/hl/test_dataset_getitem.py::TestScalarCompound::test_ellipsis Segmentation fault
```

 

 