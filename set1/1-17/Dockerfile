# TO BUILD CONTAINER RUN (inside repository)
# $ docker build -t gatsby-site-generator .

# TO RUN CONTAINER
# $ docker run -p 8000:8000 gatsby-site-generator

FROM node
RUN apt-get update && apt-get install -y curl
RUN npm install
RUN npm install -g gatsby-cli
ARG name=gatsby-site
RUN gatsby new ${name}
WORKDIR ${name}
EXPOSE 8000
CMD ["gatsby", "develop", "--host=0.0.0.0"]
