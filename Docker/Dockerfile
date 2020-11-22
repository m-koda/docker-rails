FROM ruby:2.5

RUN apt-get update && apt-get install -y \
  build-essential \
  libpq-dev \
  nodejs \
  postgresql-client \
  yarn

WORKDIR /myapp

COPY Gemfile Gemfile.lock /myapp/

RUN bundle install

CMD ["bin/rails", "server", "-b", "0.0.0.0"]