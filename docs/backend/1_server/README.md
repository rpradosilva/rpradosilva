# **Estrutura Backend**
> Precisa ter o node instalado.

## **1.** Criar Arquivo
Criar arquivo `server.js`

---

## **2.** Inicializar Node
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

> Inserir no server.js

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

### **5.3** - Criar rotas
> Necessário criar o `index.html` e/ou frontend pronto
```javascript
server.get("/", function(req, res) {
    return res.render("index")
})
```
### **5.4** - Configurar possíveis erros
```javascript
server.use(function(req, res) {
    res.status(404).render("not-found")
})
```

### **5.5** - Configurar arquivos estáticos
> Por padrão, na pasta `public`
```javascript
server.use(express.static("public"))
```
