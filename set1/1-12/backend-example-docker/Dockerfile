# TO BUILD CONTAINER RUN (inside backend repository)
# $ docker build -t backend .

# TO RUN CONTAINER
# $ docker run -p 8000:8000 -v $(pwd)/logs.txt:/app/logs.txt -d  backend


FROM node
WORKDIR /app
COPY . /app
RUN apt-get update && apt-get install -y curl
RUN npm install
EXPOSE 8000
ARG front_url=http://localhost:5000
ENV FRONT_URL=${front_url}
CMD ["npm", "start"]
