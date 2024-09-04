FROM node:lts

WORKDIR /app

COPY package*.json package-lock.json ./
COPY tsconfig.build.json ./

RUN npm install 

COPY . .

EXPOSE 3000

CMD ["npm", "run", "start:dev"]