FROM node:12-alpine AS builder-node-yarn

WORKDIR /app

RUN apk --no-cache add \
    g++ make python git \
    && yarn global add node-gyp \
    && rm -rf /var/cache/apk/*

ONBUILD ADD package.json yarn.lock /app/
ONBUILD RUN yarn --pure-lockfile