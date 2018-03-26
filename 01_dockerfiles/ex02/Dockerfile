FROM ruby

RUN apt-get update -y && apt-get upgrade -y && mkdir -p /opt/app
RUN gem install rails
RUN apt-get install nodejs -y

ONBUILD COPY . /opt/app
ONBUILD WORKDIR /opt/app
ONBUILD EXPOSE 3000

ONBUILD RUN bundle install
ONBUILD RUN rails db:migrate
ONBUILD RUN rails db:seed
