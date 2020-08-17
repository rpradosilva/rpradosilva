# **Estrutura Backend**
> Precisa ter o node instalado.

## **1.** Estruturar dados

### **1.1** - Criar arquivo de dados
Crie o arquivo `data.js`

### **1.2** - Dados
> Inserir no `data.js`

```javascript
module.exports[
    {
        id: "Estrutura aqui"
    } // Inserir Objetos
]
```

### **1.3** Importar dados
> Inserir no `server.js` (`./` = Raiz do projeto)

```javascript
const dados = require("./data")
```

### **1.4** Exibir dados na rota
> Inserir no `server.js`

```javascript
server.get("/pagina", function (req,res){
    return res.render("pagina", 
    // Dados
    {items: dados})
}
```
