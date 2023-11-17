FROM node:14

WORKDIR /usr/src/app

COPY calculadora.js ./
COPY index.html ./

RUN npm install

EXPOSE 8080

CMD ["node", "calculadora.js"]