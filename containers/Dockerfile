FROM kaixhin/cuda-torch
MAINTAINER Daniel Petti

# Install packages needed to run the demo code.
RUN apt-get update
RUN apt-get install -y libhdf5-dev cmake

RUN luarocks install qtlua

# Install torch-hdf5
RUN git clone https://github.com/deepmind/torch-hdf5.git
RUN cd torch-hdf5 && mkdir build && cd build && cmake ..
RUN cd torch-hdf5/build && make -j10 && make install

# Clone the repository.
RUN git clone https://github.com/anewell/pose-hg-demo.git
