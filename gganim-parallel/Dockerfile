FROM rocker/r-parallel

# RUN apt-get update -qq && apt-get -y install curl

#install rust 
RUN wget --no-check-certificate \
  https://static.rust-lang.org/dist/rust-1.30.0-x86_64-unknown-linux-gnu.tar.gz \ 
  && tar -xf rust-1.30.0-x86_64-unknown-linux-gnu.tar.gz \
  && rust-1.30.0-x86_64-unknown-linux-gnu/install.sh \
  && rm -rf rust-1.30.0*

RUN R -e "install.packages(c('devtools', 'tidyverse', 'gifski', 'farver', 'png', 'progress', 'rlang', 'tweenr', 'ggplot2', 'gganimate'), Ncpus=2)"

# RUN R -e "devtools::install_github('thomasp85/gganimate')"
