FROM node:alpine

RUN apk add --no-cache git && git clone https://github.com/docker-hy/backend-example-docker && \
    cd /backend-example-docker/ && npm install && npm cache clean --force && \
    adduser -D app && chown -R app $(pwd)

USER app

WORKDIR /backend-example-docker/

CMD ["npm", "start"]