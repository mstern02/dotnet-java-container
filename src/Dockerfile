FROM mcr.microsoft.com/dotnet/sdk:8.0

RUN apt-get update && apt-get install -y openjdk-17-jdk curl
RUN curl https://get.volta.sh | bash
RUN volta install node@20