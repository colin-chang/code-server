FROM codercom/code-server:latest

LABEL version="1.0" maintainer="colinchang<zhangcheng5468@gmail.com>"

ENV DOTNET_VERSION=6.0

USER root

RUN curl -o dotnet-install.sh https://dotnet.microsoft.com/download/dotnet/scripts/v1/dotnet-install.sh \
&& chmod +x dotnet-install.sh \
&& ./dotnet-install.sh -c $DOTNET_VERSION -InstallDir /var/.dotnet \
&& rm -rf dotnet-install.sh \
&& ln -s /var/.dotnet/dotnet /usr/bin/dotnet \
&& apt update \
&& apt install -y libicu-dev \
&& apt clean

USER coder
WORKDIR /home/coder/project