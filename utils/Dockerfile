ARG BASE_IMAGE
FROM $BASE_IMAGE

RUN apt update
 
RUN apt  install sudo opencl-headers -y

ENV LD_LIBRARY_PATH="/usr/local/lib64/:${LD_LIBRARY_PATH}" 


RUN mkdir -p /workspace

COPY . /workspace

WORKDIR /workspace

RUN make build 

ENTRYPOINT ["/usr/bin/memMonitor"]


