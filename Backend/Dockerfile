
FROM node:18-alpine

RUN apk add --no-cache python3 make g++ openssl

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

RUN npx prisma generate

COPY . .

EXPOSE 3000


CMD ["npm", "start"]