FROM rust:slim-buster

# install system dependencies
RUN apt-get update && apt-get install -y git make zlib1g zlib1g-dev \
	g++
# install gfatools 
RUN git clone https://github.com/lh3/gfatools
RUN cd gfatools && make && cd

# install rust-mdbg
RUN git clone https://github.com/ekimb/rust-mdbg/
RUN cd rust-mdbg && cargo build --release
