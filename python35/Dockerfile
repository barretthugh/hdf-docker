FROM python:3.5
MAINTAINER John Readey <jreadey@hdfgroup.org>
RUN pip install --upgrade pip                           ; \
    pip install numpy                                   ; \
    pip install pytz                                    ; \
    pip install requests                                ; \
    pip install psutil                                  ; \
    cd /usr/local/src                                   ; \
    git clone https://github.com/KeepSafe/aiohttp       ; \
    cd aiohttp                                          ; \
    python setup.py install                             ; \
    cd /usr/local/src                                   ; \
    git clone https://github.com/aio-libs/aiobotocore   ; \     
    cd aiobotocore                                      ; \
    python setup.py install
