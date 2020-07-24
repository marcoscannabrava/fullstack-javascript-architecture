FROM node:10
RUN mkdir -p /user/src/app
WORKDIR /user/src/app
COPY ./package*.json ./
RUN yarn
RUN yarn add global serve
COPY . ./
RUN yarn run build
EXPOSE 5000
ENTRYPOINT ["serve", "-s", "build", "-p", "5000"]
