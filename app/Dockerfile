FROM ruby:latest
RUN apt-get update -qq 
RUN apt-get install -y build-essential libpq-dev nodejs

ENV HOME /usr/src/app/

WORKDIR $HOME
ADD Gemfile* $HOME
RUN gem update bundler
RUN bundle install
RUN rm -rf $HOME/tmp/pids/server.pid

ADD . $HOME

CMD bundle exec puma -C config/puma.rb