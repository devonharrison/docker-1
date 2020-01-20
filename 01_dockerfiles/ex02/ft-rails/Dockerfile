FROM ruby:latest
RUN apt-get update &&\
    apt-get -y upgrade &&\
    gem install rails &&\
    gem install bundler &&\
    gem install rake

ONBUILD WORKDIR /opt
ONBUILD WORKDIR rails new app

ONBUILD WORKDIR /opt/app
ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed
