FROM node:20

WORKDIR /app/frontend

COPY package*.json ./
RUN npm install

COPY . .

# 🔧 Add this line before build step to fix OpenSSL issue
ENV NODE_OPTIONS=--openssl-legacy-provider

RUN npm run build

RUN npm install -g serve
EXPOSE 3000
CMD ["serve", "-s", "build", "-l", "3000"]

