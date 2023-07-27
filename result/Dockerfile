FROM node:18-alpine
ENV NODE_ENV=production

LABEL image.name="Result NodeJS"
LABEL image.version="1.0"
LABEL image.description="A Frontend application, which is responsible for the main view of the voting app."
LABEL image.author="mmaziec"

WORKDIR /result

COPY ["package.json", "package-lock.json*", "./"]

RUN npm install --production

EXPOSE 5001

COPY . .

CMD ["node", "server.js"]