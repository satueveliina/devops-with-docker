# TO BUILD CONTAINER RUN (inside repository)
# $ docker build -t frontend .

# TO RUN CONTAINER
# $docker run -p 5000:5000 frontend


FROM node
WORKDIR /app
COPY . /app
RUN apt-get update && apt-get install -y curl
RUN npm install
EXPOSE 5000
ARG api_url=http://localhost:8000
ENV API_URL=${api_url}
CMD ["npm", "start"]
