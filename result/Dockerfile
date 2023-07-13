FROM node:18-alpine
ENV NODE_ENV=production

WORKDIR /result

COPY ["package.json", "package-lock.json*", "./"]

RUN npm install --production

EXPOSE 5001

COPY . .

CMD ["node", "server.js"]