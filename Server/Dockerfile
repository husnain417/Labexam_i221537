FROM node:18-alpine

WORKDIR /app

# Copy only package.json first to install dependencies inside container
COPY package*.json ./

RUN npm install

# Now copy the rest of your app
COPY . .

EXPOSE 4000
CMD ["node", "index.mjs"]
