# EJS #

Caso já tenha iniciado um projeto em Node.js, será preciso instalar com npm o EJS. 

###  npm install ejs ###

Depois é preciso avisar qual modelo será utilizado agora.

~~~javascript

app.set('view engine', 'ejs');

~~~

### Passo a passo para instalar um projeto em node + ejs ###

* npm init -y
* npm install express ejs --save
* criar dentro da pasta raiz do arquivo, criar um arquivo app.js e inserir o conteúdo abaixo de forma manual:

~~~javascript

const express = require('express');
const app = express();


app.set('view engine', 'ejs');

app.listen(3333, () => {
    console.log('Server rodando na porta 3333')
});

~~~

Para instalar automaticamente, é possivel apenas digital o seguinte comando no terminal:

*express --views=ejs meuApp

Desse modo, todos os arquivos iniciais já serão criados e configurados. 


