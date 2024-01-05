FROM node:18-alpine

WORKDIR /app

COPY . .

RUN npm ci

RUN npm run build

EXPOSE 9151

CMD ["npm", "run", "serve"]