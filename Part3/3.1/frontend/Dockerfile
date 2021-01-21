FROM ubuntu:16.04

RUN apt-get update && apt-get install -y git && apt-get install -y curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y nodejs && node -v && npm -v && \
    git clone https://github.com/docker-hy/frontend-example-docker && \
    cd /frontend-example-docker/ && npm install -g serve && \
    npx browserslist@latest --update-db &&npm install && npm run build && \
    npm install && npm cache clean --force

WORKDIR /frontend-example-docker/

CMD ["npm", "start"]