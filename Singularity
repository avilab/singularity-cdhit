Bootstrap: docker
From: ubuntu:latest

%labels
  Maintainer tpall

%post
apt-get update && apt-get -y install \
  wget \
  build-essential \
  git \
  zlib1g-dev \
  ncbi-blast+ \
  python3.7

git clone https://github.com/tpall/cdhit.git \
  && cd cdhit \
  && git checkout install/psi-cd-hit \
  && make \
  && make install \
  && cd cd-hit-auxtools \
  && make

## Clean up
apt-get clean \
  && rm -rf /var/lib/apt/lists/ 
cd / \
  && rm -rf cdhit

%environment
  export PATH=/usr/local/bin:$PATH
  export LC_ALL=C
