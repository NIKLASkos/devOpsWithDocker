FROM node:16.20.2

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build

EXPOSE 5000

RUN npm install -g serve

CMD ["serve", "-s", "-l", "5000", "build"]