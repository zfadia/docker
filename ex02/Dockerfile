FROM 			ruby

MAINTAINER 		fadia <fadia@alphaconcept.net>
 
 EXPOSE 		3000:3000 

 WORKDIR 		home/teamspeak 

 RUN			apt-get update
 RUN 			apt-get upgrade -y
 RUN			apt-get install -y wget bzip2 
 RUN			wget https://github.com/rbenv/rbenv

ENTRYPOINT			COPY 	app /opt/app
					WORKDIR	opt/app

