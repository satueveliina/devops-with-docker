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
ENV API_URL=http://localhost:8000
CMD ["npm", "start"]
