FROM ioft/i386-ubuntu:16.04
MAINTAINER Jonne Haß <me@jhass.eu>

RUN apt-get update && \
apt-get install -y apt-transport-https curl build-essential pkg-config libssl-dev llvm libedit-dev libgmp-dev libxml2-dev libyaml-dev libreadline-dev git-core binutils-dev libcurl4-openssl-dev zlib1g-dev libdw-dev libiberty-dev cmake python

RUN curl https://dist.crystal-lang.org/apt/setup.sh | bash && \
apt-get update && \
apt-get install -y crystal && \
\
git clone https://github.com/SimonKagstrom/kcov /tmp/kcov && \
cd /tmp/kcov && \
git checkout v33 && \
\
mkdir build && cd build && \
cmake -DCMAKE_BUILD_TYPE=Release .. && \
make && \
make install && \
\
cd / && \
rm -Rf /tmp/kcov

CMD ["/bin/bash"]
