FROM node:18.0.6-alpine

WORKDIR /usr/src/app

COPY package.json .

COPY yarn.lock .

RUN yarn

COPY . .

RUN yarn build

RUN npm install -g serve

CMD [ "serve", "-s", "build" ]