FROM node:10
RUN mkdir -p /user/src/app
WORKDIR /user/src/app
COPY ./package*.json ./
RUN yarn
COPY . ./
RUN yarn run build:prod
EXPOSE 8000
ENTRYPOINT ["node", "build/index.js"]
