FROM node:24-alpine AS build

WORKDIR /usr/src/app

COPY package*.json ./
RUN npm ci

COPY . .
RUN npm run build

FROM node:24-alpine

WORKDIR /usr/src/app

RUN npm install -g serve@14.2.5

COPY --from=build --chown=node:node /usr/src/app/dist ./dist

USER node

EXPOSE 3000

CMD ["serve", "-s", "dist", "-l", "3000"]
