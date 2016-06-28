FROM m0elnx/ubuntu-32bit
MAINTAINER Jonne Haß <me@jhass.eu>

RUN apt-get update && \
apt-get install -y curl build-essential pkg-config libssl-dev llvm-3.6 libedit-dev libgmp-dev libxml2-dev libyaml-dev libreadline-dev git-core && \
curl https://dist.crystal-lang.org/apt/setup.sh | bash && \
apt-get update && \
apt-get install -y crystal

CMD ["/bin/bash"]
