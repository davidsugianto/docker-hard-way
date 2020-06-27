FROM node:12-alpine AS builder

LABEL maintainer David Sugianto <idiots718@gmail.com>

ENV BUILD_FLAG ${BUILD_FLAG} \
    NODE_PORT ${NODE_PORT}

RUN apk add --no-cache git && npm install pm2@latest -g

WORKDIR /app/nuxt

COPY .nuxt/ ./.nuxt/
COPY server/ ./server/
COPY static/ ./static/
COPY node_modules/ ./node_modules/
COPY ecosystem.config.js nuxt.config.js package.json package-lock.json ./

EXPOSE ${NODE_PORT}

CMD [ "sh", "-c", "npm run start:$BUILD_FLAG" ]
