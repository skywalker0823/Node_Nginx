FROM node:14.17.3-alpine3.14

WORKDIR /usr/src/app

COPY package.json package-lock.json ./
RUN npm ci
RUN npm install pm2 -g
COPY ./server.js ./


CMD ["pm2-runtime", "npm", "--", "start"]
