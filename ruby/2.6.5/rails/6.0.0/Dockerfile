FROM ruby:2.6.5
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash -
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
RUN apt-get update -y && apt-get install -y nodejs yarn
RUN gem install -N rails:6.0.0
COPY ruby/2.6.5/rails/6.0.0/Gemfile* ./
RUN bundle install --jobs 8
