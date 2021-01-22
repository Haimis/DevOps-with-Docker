FROM node:alpine as prebuild

RUN apk add --no-cache git && git clone https://github.com/docker-hy/frontend-example-docker && \
    cd /frontend-example-docker/ && \
    npm install && npm run build && npm run build

FROM node:alpine

COPY --from=prebuild /frontend-example-docker/dist ./dist

RUN npm install -g serve

CMD serve -s -l 5000 dist