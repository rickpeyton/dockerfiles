FROM ruby:2.5.3
RUN gem install -N rails:5.2.3
RUN apt-get -y update && \
    apt-get -y install \
      gifsicle \
      jhead \
      jpegoptim \
      nodejs \
      optipng \
      brotli
RUN gem update --system && gem install -N bundler -v '1.17.3'
