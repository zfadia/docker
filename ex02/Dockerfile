FROM 			ruby

MAINTAINER 		fadia <fadia@alphaconcept.net>

ENV 			TS3SERVER_LICENSE=accept
 
 EXPOSE 		3000:3000 

 WORKDIR 		home/teamspeak 

 RUN			apt-get update
 RUN 			apt-get upgrade -y
 RUN			apt-get install -y wget bzip2 
 RUN			wget https://github.com/rbenv/rbenv

CMP				cp ruby mycontainer:/opt/app





FROM ruby
RUN apt-get update -y && apt-get install -y build-essential libpq-dev nodejs sqlite3

MAINTAINER fadia <fadia@alphaconcept.net>

ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD EXPOSE 3000
ONBUILD RUN bundle install
ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed
