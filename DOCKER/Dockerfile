FROM ruby:3.1.2
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs
ENV APP_HOME /budget-app
RUN mkdir $APP_HOME
WORKDIR $APP_HOME
COPY Gemfile Gemfile.lock ./
RUN gem install bundler:2.3.6
RUN bundle install
COPY . .
EXPOSE 3000
CMD ["rails", "server", "-b", "0.0.0.0"]
