# TO BUILD CONTAINER RUN (inside frontend repository)
# $ docker build -t frontend .

# TO RUN CONTAINER
# $ docker run -p 5000:5000 frontend


FROM ubuntu:16.04
WORKDIR /app
COPY . /app
RUN apt-get update && apt-get install -y curl && curl -sL https://deb.nodesource.com/setup_10.x | bash && apt-get install -y nodejs
RUN npm install
EXPOSE 5000
CMD ["npm", "start"]
