# FROM node:12 as BUILD
# WORKDIR /app
# COPY . .
# RUN npm install
# RUN npm run build --prod

#stage 2
WORKDIR /app
COPY . .
FROM nginx:alpine
COPY /app/dist/taskZero /usr/share/nginx/html
EXPOSE 80