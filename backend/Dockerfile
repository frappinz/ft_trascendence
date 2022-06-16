FROM node:14-alpine
RUN mkdir -p /usr/src/
WORKDIR /usr/src/
RUN npm i -g @nestjs/cli --silent
COPY package.json .
COPY package-lock.json .
RUN npm install --silent
COPY . .
# Value set in .env file.
EXPOSE $BACKEND_PORT
CMD ["npm", "run", "start:dev"]