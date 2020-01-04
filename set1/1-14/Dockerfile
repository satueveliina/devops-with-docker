# TO BUILD CONTAINER RUN (inside repository)
# $ docker build -t rails-app .

# TO RUN CONTAINER
# $ docker run -p 3000:3000 -d  rails-app


FROM ruby:2.6.0
WORKDIR /app
COPY . /app
RUN bundle update --bundler
RUN bundle install
RUN apt-get update && apt-get install -y curl && curl -sL https://deb.nodesource.com/setup_10.x | bash && apt-get install -y nodejs
RUN bin/rails db:migrate
EXPOSE 3000
CMD ["bin/rails", "s"]
