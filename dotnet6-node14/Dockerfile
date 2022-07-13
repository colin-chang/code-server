FROM colinchang/code-server:dotnet6

LABEL version="4.5.0" maintainer="colinchang<zhangcheng5468@gmail.com>"

ENV NODE_VERSION=14

USER root

RUN curl -sL https://deb.nodesource.com/setup_$NODE_VERSION.x | bash - \
&& apt update \
&& apt install -y nodejs \
&& apt clean

USER coder
WORKDIR /home/coder/project