# base image
FROM node:9.11

# set working directory

COPY /* /var/www/_react/
WORKDIR /var/www/_react

# add `/usr/src/app/node_modules/.bin` to $PATH
ENV PATH /var/www/_react/node_modules/.bin:$PATH

# install and cache app dependencies
COPY package.json /var/www/_react/package.json

RUN npm install

RUN npm rebuild node-sass
RUN npm install caniuse-lite browserslist

# start app
EXPOSE 5000
CMD ["node", "server"]
