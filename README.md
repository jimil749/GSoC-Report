<img src="./img/GSOC.jpg" alt="GSoC Logo"/>


# Runtime Plugin Ecosystem Support for oCIS
### By: Jimil Desai

## About Me


Hey there! I am Jimil Desai, B.Tech Information and Communication Technology student at School of Engineering and Applied Science, Ahmedabad University. This repository contains a summary of work done by me during Google Summer of Code 2021 under CERN-HSF.

## Special thanks to my Mentors and the REVA Community

First off, I would like to thank my mentors and the entire CS3 community for helping me throughout the journey and making me a better software developer in the process

- [Ishank Arora](https://github.com/ishank011)
- [Hugo Labrador](https://github.com/labkode)
- [Alex Unger](https://github.com/refs)
- [Michael Usher](https://github.com/mdusher)


## Aim

The project aims to add Runtime pluggability to the Reva framework in order to improve overall developer experience. This enhancement would allow plugins to be loaded at runtime in Reva.

## Work Summary

1. [Go-Plugin Benchmarking](https://github.com/jimil749/reva-plugin-benchmark)

    - Performed Benchmarking for various go-plugin framework to analyse, compare and select the best plugin framework for our case.
    - Packages Benchmarked:
        - [Hashicorp go-plugin](https://github.com/hashicorp/go-plugin)
        - [Natefinch pie-plugin](https://github.com/natefinch/pie)
        - [Native golang Plugin](https://golang.org/pkg/plugin/)
        - [Traefik Yaegi](https://github.com/traefik/yaegi)
        - [Goloader](https://github.com/pkujhd/goloader)
    - Used the existing `JSON` plugin from `userprovider` service for Benchmarking purposes.