FROM node:18-alpine

# Defina o diretório de trabalho no container
WORKDIR /app

# Copie o arquivo package.json e package-lock.json
COPY package*.json ./

# Instale as dependências do projeto
RUN npm install

# Copie o restante do código da aplicação
COPY . .

# Instale o Nodemon para monitoramento de arquivos
RUN npm install -g @nestjs/cli nodemon

# Exponha a porta em que o Nest.js roda (geralmente 3000)
EXPOSE 3000

# Comando padrão para iniciar o container no modo watch
CMD ["npm", "run", "start:dev"]