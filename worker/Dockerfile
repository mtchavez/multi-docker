FROM node:alpine

ENV APP_DIR /app
WORKDIR $APP_DIR
COPY package.json .
RUN npm i
COPY . .

CMD ["npm", "run", "start"]
