FROM debian

MAINTAINER 	fadia <fadia@alphaconcept.net>

ENV TS3SERVER_LICENSE=accept
 
EXPOSE 		9987/udp 10011 30033 

WORKDIR 	home/teamspeak 

RUN			apt-get update
RUN 		apt-get upgrade -y
RUN			apt-get install -y wget bzip2 
RUN			wget https://files.teamspeak-services.com/releases/server/3.9.1/teamspeak3-server_linux_amd64-3.9.1.tar.bz2
RUN			tar xvfj teamspeak3-server_linux_amd64-3.9.1.tar.bz2

WORKDIR 	teamspeak3-server_linux_amd64

ENTRYPOINT 	sh ts3server_minimal_runscript.sh

