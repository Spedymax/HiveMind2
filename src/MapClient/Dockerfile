# етап 1 ‒ збірка frontend
FROM node:20-alpine AS build
WORKDIR /app
COPY package*.json ./
RUN npm ci
COPY . .
EXPOSE 3000
ENTRYPOINT ["npm", "run", "dev"]

