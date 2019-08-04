FROM parallel-ver:3.6.1

RUN apt-get update -qq && apt-get -y --no-install-recommends install \
  libcurl4-openssl-dev \ # originally in rocker/rstudio
  libssl-dev \ # originally in rocker/rstudio
  libxml2-dev \
  libcairo2-dev \
  libsqlite3-dev \
  libmariadbd-dev \
  libmariadb-client-lgpl-dev \
  libpq-dev \
  libssh2-1-dev \
  unixodbc-dev \
  libsasl2-dev \
  && install2.r --error \
    --deps TRUE \
    tidyverse \
    dplyr \
    devtools \
    formatR \
    remotes \
    selectr \
    caTools \
    BiocManager \
    aws.s3


