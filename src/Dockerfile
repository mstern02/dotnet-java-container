FROM mcr.microsoft.com/dotnet/sdk:8.0

RUN apt-get update && apt-get install -y openjdk-17-jdk curl xz-utils rsync
RUN NODE_VERSION="node-v20.17.0-linux-x64" && curl "https://nodejs.org/dist/v20.17.0/${NODE_VERSION}.tar.xz" > /tmp/node.tar.xz && cd /tmp && tar xf node.tar.xz && cd $NODE_VERSION && echo "bin\nlib\ninclude\nshare" | xargs -rI{} rsync -a "{}/" "/{}"