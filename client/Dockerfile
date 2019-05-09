FROM node:alpine as BUILD

ENV APP_DIR /app
WORKDIR $APP_DIR
COPY package.json .
RUN npm i
COPY . .
CMD ["npm", "run", "build"]

FROM nginx
EXPOSE 3000

COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=BUILD /app/build /usr/share/nginx/html
