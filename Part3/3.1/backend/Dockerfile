FROM ubuntu:16.04

RUN apt-get update && apt-get install -y git && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y nodejs && \
    node -v && npm -v && \
    git clone https://github.com/docker-hy/backend-example-docker && \
    cd /backend-example-docker/ && npm install && npm cache clean --force

WORKDIR /backend-example-docker/

CMD ["npm", "start"]