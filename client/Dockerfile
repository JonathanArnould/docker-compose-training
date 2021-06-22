FROM node:current-alpine3.10

RUN mkdir /client
WORKDIR /client

ENV PATH /app/node_modules/.bin:$PATH

COPY package.json ./
COPY yarn.lock ./

RUN yarn install

COPY src src
COPY public public

CMD ["yarn", "start"]
