# tecnologia usada (desktop)

- eletron.js
- node.js
- html5
- css3
- javaScript
- jason
- socket


# dependencias

- express
- ejs
- path
- body-parser
- mysql
- socket

use o seguinte codigo para instalar as dependencias necessarias

```bash
    npm install express ejs path body-parser mysql2
```


# inicio rápido

para criar o arquivo package.json responsavel por funções do back-end


```bash
    npm init
```


crie um arquivo "index.js" e declare as seguintes dependencias e constantes a serem usadas no decorrer do projeto

```javascript
const express = require('express');
const path = require('path');
const port = 3535;
const app = express();
const mysql = require('mysql2');
const bodyParser = require('body-parser');
```

agora precisamos declarar os caminhos do express, ejs e path

```javascript
app.engine('html', require('ejs').renderFile);
app.set('view engine', 'html');
app.use('/public', express.static(path.join(__dirname, 'public')));
app.set('views', path.join(__dirname, '/views'));
```

é necessario criar duas pastas dentro do seu projeto "views" e "public" a pasta "views" fica os arquivos estaticos, .html e no "public" arquivos como .css .img e afins 

seu diretorio deve se assemelhar a isso:

.

-main
  - node_modules
  - public
    - .css
    - .img
  - views
    - .html
  - index.js
  - package.json
  - package-lock.json


definido as rotas e caminhos dos arquivos estaticos precisamos declarar o body-parser

```javascript
app.use(bodyParser.json());
app.use(bodyParser.urlencoded({extended:true}));
```

por fim temos que abrir o servidor

```javascript
app.listen(port, () => {console.log(`Servidor rodando em localhost:{port}`);});
```

agora podemos rodar o comando para abrir o servidor local

```bash 
    node index.js
```

agora vc pode abrir uma pagina no seu navegador de preferencia e ir no link do [localhost:3535](localhost:3535)

```bash 

    // BÁSICOS

      git init

      git add .

      git status

      git commit -m (...)


    // ADICIONAR

      git push origin (...)
      
    // MUDAR DIRETÓRIO

      git checkout (...)

    // ATUALIZAR

      git pull

    // CLONAR
  
      git clone


```
