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

Link to Project: https://github.com/cs3org/reva/projects/2
    
1. [Go-Plugin Benchmarking](https://github.com/jimil749/reva-plugin-benchmark)

    - Performed Benchmarking for various go-plugin framework to analyse, compare and select the best plugin framework for our case.
    - Packages Benchmarked:
        - [Hashicorp go-plugin](https://github.com/hashicorp/go-plugin)
        - [Natefinch pie-plugin](https://github.com/natefinch/pie)
        - [Native golang Plugin](https://golang.org/pkg/plugin/)
        - [Traefik Yaegi](https://github.com/traefik/yaegi)
        - [Goloader](https://github.com/pkujhd/goloader)
    - Used the existing `JSON` plugin from `userprovider` service for Benchmarking purposes.

2. [Plugin Package](https://github.com/cs3org/reva/pull/1861)

    - Finalized the plugin framework after discussion with the mentors. Selected Framework: Hashicorp's [go-plugin](https://github.com/hashicorp/go-plugin) over RPC.
    - Introduced Plugin package in the Reva codebase, which supports loading plugins at runtime.
    - Ensured minimal changes in the configuration for backwards compatibility.
    - Migrated the existing in-memory `JSON` driver from the `userprovider` service to runtime paradigm.
    - Supported 3 ways of loading plugins:
        - Load already compiled binary
        - Compile the source code and load the binary
        - Load plugins from in-memory registry

3. [Enable fetching plugins from github](https://github.com/cs3org/reva/pull/1970)

    - Added a new feature to download, compile and load plugins hosted on Github.
    - User can specify multiple protocols to download the source code.

4. [Methods to get and set context](https://github.com/cs3org/reva/pull/1938)

    - Created methods, `GetContextKV` to extract context values from context and `PutContextKV` to put context values into context type.

5. [Migrated User/Token context methods into Separate package](https://github.com/cs3org/reva/pull/1982)

    - Refractored the code base by separating the user and token context methods into a separate package.
    - Used to "Get" and "Set" user and token context.
    - Used by RPC packages to send context data over RPC to plugins.

6. [Documentation](https://github.com/cs3org/reva/pull/1971)

    - Added basic developer manual/documention describing the Reva plugin architecture.
    - Documentation serves as guide for the reva plugin developers.

7. [Blog](https://gsoc-blog.netlify.app/)

    - Maintained a blog describing my weekly work and my entire journey, check it out if you are more interested in my work! :)

### Pre-GSoC

1. [Make commands to run litmus-tests](https://github.com/cs3org/reva/pull/1543)

    - My first contribution to Reva project.
    - Added `Make` command to run litmus tests which provided an easy way to run litmus tests.

2. [OCM Invitation Workflow Commands](https://github.com/cs3org/reva/pull/1558)

    - Added CLI commands:
        - `ocm-invite-generate`: to generate an invitation token
        - `ocm-invite-forward`:  to forward the invitation token to the mesh provider

3. [Modularized API Token Management](https://github.com/cs3org/reva/pull/1574)

    - Refractored the GRAPPA Driver code to remove code duplication.

**Note: All of these PRs are not merged yet.**

## Contact

- [LinkedIn](https://www.linkedin.com/in/jimil-desai/)
- [Github](https://github.com/jimil749)
- [Portfolio](http://jimil-desai.s3-website.ap-south-1.amazonaws.com/)
- [Email](jimildesai42@gmail.com)
