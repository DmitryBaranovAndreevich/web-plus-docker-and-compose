FROM node:16-alpine AS builder
WORKDIR /app
COPY package*.json .
RUN npm install
COPY . .
RUN npm install
RUN npm run build
# RUN sudo mkdir -p /var/www/certbot/

FROM nginx:latest AS frontend
COPY --from=builder /app/build /usr/share/nginx/html
EXPOSE 80
EXPOSE 443
CMD ["nginx", "-g", "daemon off;"]

