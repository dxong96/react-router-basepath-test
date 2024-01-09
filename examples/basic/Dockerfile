FROM node:18-alpine

WORKDIR /app

COPY . .

RUN npm ci

RUN npm run build

FROM nginx:mainline-alpine

WORKDIR /app

COPY --from=0 /app/dist .

COPY nginx.conf /etc/nginx/nginx.conf

EXPOSE 9151