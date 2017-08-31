FROM node:6.9
MAINTAINER jairofdezvega@gmail.com
LABEL authors="Jairo Fdez <jairofdezvega@gmail.com>"

# prepare a user which runs everything locally! - required in child images!
RUN useradd --user-group --create-home --shell /bin/false app

ENV HOME=/usr/src/app
RUN mkdir $HOME
WORKDIR $HOME

RUN npm install -g @angular/cli && npm cache clean

EXPOSE 4200
EXPOSE 49153
EXPOSE 9876