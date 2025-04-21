FROM node:18-alpine

WORKDIR /app
COPY package.json package-lock.json ./

RUN npm install
COPY . .

RUN npm start

FROM nginx:alpine

COPY --from=0 /app/build /usr/share/nginx/html

EXPOSE 3000
CMD ["nginx", "-g", "daemon off;"]