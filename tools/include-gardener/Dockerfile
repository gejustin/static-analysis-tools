FROM gcc:latest as core-install
RUN wget https://github.com/Kitware/CMake/releases/download/v3.24.2/cmake-3.24.2.tar.gz
RUN tar -zxvf cmake-3.24.2.tar.gz
WORKDIR /cmake-3.24.2
RUN ls
RUN ./bootstrap
RUN make
RUN make install
RUN cmake --version
RUN apt update
RUN apt install --yes build-essential libboost-system-dev libboost-thread-dev libboost-program-options-dev libboost-test-dev libboost-log-dev

FROM core-install
WORKDIR /root
RUN git clone https://github.com/feddischson/include_gardener.git
WORKDIR /root/include_gardener
RUN sed -i 's/master/main/g' CMakeLists.txt.in
RUN mkdir build
WORKDIR /root/include_gardener/build
RUN cmake ..
RUN make
# RUN make doc
RUN make install
ENV PATH="/root/include_gardener/build:$PATH"

ENTRYPOINT [ "include_gardener" ]
