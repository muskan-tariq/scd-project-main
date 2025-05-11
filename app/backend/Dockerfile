FROM node:20
WORKDIR /app/backend
COPY package*.json ./
RUN yarn
COPY . .
EXPOSE 5000
CMD ["node", "server.js"]
