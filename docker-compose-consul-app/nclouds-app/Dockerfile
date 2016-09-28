FROM node:argon

# Clone git repo
RUN git clone https://github.com/rgupta993/nclouds-app.git /opt

WORKDIR /opt
ENV NODE_ENV production

# Install app dependencies
RUN npm install

EXPOSE 4000
CMD node app.js
