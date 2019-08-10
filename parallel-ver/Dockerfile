## Emacs, make this -*- mode: sh; -*-

# Heavily copied from rocker/parallel

FROM rocker/r-ver:3.6.1

MAINTAINER "Mark Hagemann" mark.hagemann@gmail.com

## System libraries
RUN apt-get update \
    && apt-get install -y \
       libopenmpi-dev \
       libzmq3-dev

## Legacy (snow is deprecated)
RUN install2.r snow doSNOW 

## MPI
## RUN install2.r Rmpi

## Random Number Generation (RNG)
RUN install2.r rlecuyer

## The foreach ecosystem
RUN install2.r foreach iterators
RUN install2.r doParallel doMC doRNG

## The future ecosystem
RUN install2.r future
RUN install2.r future.apply
RUN install2.r doFuture
RUN install2.r future.callr
RUN install2.r furrr

RUN install2.r BatchJobs future.BatchJobs   ## heavy set of dependencies
RUN install2.r batchtools future.batchtools ## heavy set of dependencies
RUN install2.r clustermq                    ## heavy set of dependencies

