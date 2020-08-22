# **Estrutura Backend**: Servidor

[![](https://img.shields.io/badge/1.-Criar%20Arquivo-4969D7?style=flat-square&labelColor=21275C)](#1-criar-arquivo)
[![](https://img.shields.io/badge/2.-Inicializar%20Node-4969D7?style=flat-square&labelColor=21275C)](#2-inicializar-node)
[![](https://img.shields.io/badge/3.-Instalar%20Dependências-4969D7?style=flat-square&labelColor=21275C)](#3-instalar-dependências)
[![](https://img.shields.io/badge/4.-Configurar%20package.json-4969D7?style=flat-square&labelColor=21275C)](#4-configurar-packagejson)
[![](https://img.shields.io/badge/5.-Configurar%20Servidor-4969D7?style=flat-square&labelColor=21275C)](#5-configurar-servidor)
[![](https://img.shields.io/badge/6.-Configurar%20Rotas-4969D7?style=flat-square&labelColor=21275C)](#6-configurar-rotas)
___

## **1.** Criar Arquivo
Criar arquivo `server.js`

---

## **2.** Inicializar Node
> Precisa ter o node instalado.

`npm init` - Necessário configurar projeto

`npm init -y` - Inicializar rapidamente com configurações padrão

---

## **3.** Instalar Dependências
`npm install express` - Necessário para construir o servidor

`npm install nunjucks` - Necessário para deixar o conteúdo dinâmico *(Template Engine)*

`npm install -D nodemon` - Necessário para automatizar a atualização do servidor. O *-D* para dependência de desenvolvedor.

---

## **4.** Configurar `package.json`

Configurar debug do servidor no arquivo `package.json`
```json
{
"scripts": {
        "start": "nodemon server.js"
    }
}
```

---

## **5.** Configurar Servidor

> Inserir no `server.js`

### **5.1** - Importar express
```javascript
const express = require("express")
const server = express()
```

### **5.2** - Configurar debug e porta
> Deixar link para acesso rápido via terminal
```javascript
const port = 5000

server.listen(port, function() {
    console.log(`Server is running in: http://localhost:${port}`)
})
```

### **5.3** - Configurar arquivos estáticos
> Por padrão, na pasta `public`
```javascript
server.use(express.static("public"))
```

### **5.4** - Status (Erro 404)
```javascript
server.use(function(req, res) {
    res.status(404).render("not-found")
})
```
---

## **6.** Configurar Rotas
> Inserir no `routes.js`

### **6.1** - Importar express
```javascript
const express = require("express")
const routes = express.Router()
```

### **6.2** - Criar rotas
```javascript
routes.get("/", function(req, res) {
    return res.render("index")
})
```

### **6.3** - Exportar rotas
```javascript
module.exports = routes
```

### **6.4** - Importar rotas no `server.js`
```javascript
const routes = require("./routes")

server.use(routes)
```

### **6.5** - Redirecionamento de rotas
```javascript
routes.get("/", function(req, res) {
    return res.redirect("/teachers")
})
```
### **6.6** - Transmitindo dados nas rotas

**Query Strings**
> Configurar URL: `?id=#####`
```javascript
server.get("/video", function(req, res) {
    // selecionar o id na url
    const id = req.query.id
    // procurar o array de videos do data.js
    const video = videos.find(
        // comparar o id do vídeo com a url
        function (video){ return video.id == id }
    )
    // se o vídeo não existir
    if (!video) {
        return res.send("Vídeo não encontrado.")
    }
    // renderiza a estrutura com os
    return res.render("video", {item: video})
})
```
**Parametros (com base nos dados)**
> Configurar URL: `/:id`
```javascript
server.get("/recipes/:index", function (req, res) {
  const recipes = [...]; // Array de receitas carregadas do data.js
  const recipeIndex = req.params.index;

  console.log(recipes[recipeIndex]);
})
```

> **IMPORTANTE:** Em todos os casos é necessário fazer o redirect da URL do botão, após concluir esta configuração