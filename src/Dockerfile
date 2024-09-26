ARG DOTNET_VERSION="8.0"

FROM mcr.microsoft.com/dotnet/sdk:$DOTNET_VERSION
ARG NODE_VERSION="v20.17.0"

RUN apt-get update && apt-get install -y openjdk-17-jdk curl xz-utils rsync
RUN curl -L "https://nodejs.org/dist/${NODE_VERSION}/node-${NODE_VERSION}-linux-x64.tar.xz" > /tmp/node.tar.xz && cd /tmp && tar xf node.tar.xz && cd node-${NODE_VERSION}-linux-x64 && echo "bin\nlib\ninclude\nshare" | xargs -rI{} rsync -a "{}/" "/{}"
