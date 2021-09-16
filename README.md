# rust-mdbg-docker

This repository contains a Dockerfile to build [rust-mdbg: Minimizer-space de Bruijn graphs (mdBG) for whole-genome assembly](https://github.com/ekimb/rust-mdbg/) with [gfatools](https://github.com/lh3/gfatools/). 

The Docker container is built using the official Rust `rust:slim-buster` container as the base image. And is available on Dockerhub [here](https://hub.docker.com/repository/docker/rbartelme/rust-mdbg).

If you use this Docker container image, please cite the original authors of `rust-mdbg`:

```
@article {mdbg,
	author = {Ekim, Bar{\i}{\c s} and Berger, Bonnie and Chikhi, Rayan},
	title = {Minimizer-space de Bruijn graphs: Whole-genome assembly of long reads in minutes on a personal computer},
	journal = {Cell Systems},
	year = {2021},
	issn = {2405-4712},
	doi = {https://doi.org/10.1016/j.cels.2021.08.009}
}

```


