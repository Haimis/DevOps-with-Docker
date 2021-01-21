FROM node:alpine

RUN apk add --no-cache git && git clone https://github.com/docker-hy/frontend-example-docker && \
    cd /frontend-example-docker/ && npm install -g serve && \
    npx browserslist@latest --update-db &&npm install && npm run build && \
    npm install && npm cache clean --force && adduser -D app && chown -R app $(pwd)

USER app

WORKDIR /frontend-example-docker/

CMD ["npm", "start"]