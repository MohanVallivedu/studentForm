
# FROM node:12 as BUILD
# WORKDIR /app
# COPY . .
# RUN npm install
# RUN npm run build --prod
# FROM nginx:alpine
# COPY --from=BUILD /app/dist/taskZero /usr/share/nginx/html
# EXPOSE 80

FROM node:12 as node
WORKDIR /app
COPY package.json .
RUN npm i npm@latest -g
RUN npm install
RUN npm install -g @angular/cli
COPY . .
RUN npm run build

#Stage 2
FROM nginx:1.13.12-alpine
#COPY --from=node /usr/src/app/dist/taskZero /usr/share/nginx/html
VOLUME /app/dist/taskZero:/usr/share/nginx/html
EXPOSE 80

#COPY ./nginx.conf /etc/nginx/conf.d/default.conf