FROM ruby:4.0.0

RUN apt-get update -qq && apt-get install -y nodejs

COPY Gemfile /app/Gemfile

WORKDIR /app

RUN bundle install

# Add a script to be executed every time the container starts.
COPY entrypoint.sh /usr/bin/

RUN chmod +x /usr/bin/entrypoint.sh

ENTRYPOINT ["entrypoint.sh"]
EXPOSE 9000
