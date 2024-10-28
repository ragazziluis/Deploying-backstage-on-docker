# Use a imagem Node.js como base
FROM node:14-buster-slim

# Defina o diretório de trabalho
WORKDIR /app

# Copie o package.json e o yarn.lock para o contêiner
COPY package.json yarn.lock ./

# Instale as dependências
RUN yarn install --frozen-lockfile

# Copie o restante dos arquivos para o contêiner
COPY . .

# Compilação do Backstage
RUN yarn build

# Exponha a porta 7000
EXPOSE 7000

# Comando para iniciar o Backstage
CMD ["yarn", "start"]
