FROM ruby:2.5.3
RUN gem install -N rails:5.2.3
RUN apt-get -y update && \
    apt-get -y install \
      brotli \
      gifsicle \
      jhead \
      jpegoptim \
      nodejs \
      optipng \
      postgresql-client
RUN gem update --system && gem install -N bundler -v '1.17.3'
