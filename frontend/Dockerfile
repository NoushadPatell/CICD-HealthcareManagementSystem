# Build Stage
FROM node:20-alpine as build
WORKDIR /app
COPY . .
RUN npm install && npm run build

# Serve Stage
FROM nginx:stable-alpine
COPY --from=build /app/build /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]

