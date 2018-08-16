FROM ruby

MAINTAINER dtelega <dtelega@student.unit.ua>

RUN apt-get update -yq && apt-get install -yq build-essential libpq-dev nodejs sqlite3

ENV RAILS_ENV=production

ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD EXPOSE 3000
ONBUILD RUN bundle install
ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed
