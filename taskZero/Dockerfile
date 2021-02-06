FROM node:12 as BUILD
WORKDIR /app
COPY . .
RUN npm install
RUN npm run build --prod

#stage 2
FROM nginx:alpine
COPY --from=BUILD /app/dist/taskZero /usr/share/nginx/html