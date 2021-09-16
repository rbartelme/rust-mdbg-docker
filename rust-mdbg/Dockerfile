FROM rust:slim-buster

# install system dependencies
RUN apt-get update && apt-get install -y git make zlib1g zlib1g-dev \
	g++
# install gfatools 
RUN git clone https://github.com/lh3/gfatools
RUN cd gfatools && make
RUN cd

# install rust-mdbg
RUN git clone https://github.com/ekimb/rust-mdbg/
RUN cd rust-mdbg && cargo build --release
RUN cd

# create aliases for programs

# gfatools
RUN echo 'alias gfatools="/gfatools/gfatools"' >> ~/.bashrc

# rust-mdbg
RUN echo 'alias rust-mdbg="/rust-mdbg/target/release/rust-mdbg"' >> ~/.bashrc

# magic_simplify
RUN echo 'alias magic_simplify="/rust-mdbg/utils/magic_simplify"' >> ~/.bashrc

# multi k assembly
RUN echo 'alias multik="/rust-mdbg/utils/multik"' >> ~/.bashrc

# to basespace
RUN echo 'alias to_basespace="/rust-mdbg/target/release/to_basespace"' >> ~/.basrhc

#set bash as entrypoint
ENTRYPOINT ["bash"]
