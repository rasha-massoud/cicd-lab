FROM node:22-alpine

WORKDIR /app

# Update npm inside the image to fix bundled npm dependency vulnerabilities
RUN npm install -g npm@latest

COPY package*.json ./
RUN npm ci --omit=dev

COPY server.js .

EXPOSE 3000
CMD ["npm", "start"]