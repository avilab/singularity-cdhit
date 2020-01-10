Bootstrap: docker
From: ubuntu:latest

%labels
  Maintainer tpall
  CD-HIT_Version 4.8.1

%post
apt-get update && apt-get -y install \
  wget \
  build-essential \
  zlib1g-dev \
  ncbi-blast+

wget -q  https://github.com/weizhongli/cdhit/releases/download/V4.8.1/cd-hit-v4.8.1-2019-0228.tar.gz \
  && tar xvf cd-hit-v4.8.1-2019-0228.tar.gz --gunzip \
  && cd cd-hit-v4.8.1-2019-0228 \
  && make \
  && cd cd-hit-auxtools \
  && make

## Clean up
  apt-get clean \
  && rm -rf /var/lib/apt/lists/
