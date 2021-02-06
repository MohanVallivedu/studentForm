# FROM node:12
# WORKDIR /app
# COPY . .
# RUN npm install
# RUN npm install -g nodemon
# EXPOSE 3000
# CMD ["nodemon","index.js"]


FROM node:12
RUN mkdir -p /app
WORKDIR /app
COPY . .
RUN npm install
RUN npm install -g nodemon
EXPOSE 3000
CMD ["nodemon", "index.js"]