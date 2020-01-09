FROM debian:latest
ENV TEAMSPEAK_SERVER_LICENSE=accept
WORKDIR /teamspeak3
RUN apt-get update -y &&\
    apt-get upgrade -y &&\
    apt-get install -y wget bzip2 &&\
    wget http://dl.4players.de/ts/releases/3.8.0/teamspeak3-server_linux_amd64-3.8.0.tar.bz2 &&\
    tar -xvf teamspeak3-server_linux_amd64-3.8.0.tar.bz2
WORKDIR teamspeak3-server_linux_amd64
ENTRYPOINT ./ts3server_startscript.sh start
