# **Estrutura Backend**: Dados

[![](https://img.shields.io/badge/1.-Estruturar%20dados-4969D7?style=flat-square&labelColor=21275C)](#1-estruturar-dados)

---

## **1.** Estruturar dados

### **1.1** - Criar arquivo de dados

Crie o arquivo `data.js`

### **1.2** - Dados

> Inserir no `data.js`

```javascript
module.exports[
  {
    id: "Estrutura aqui",
  } // Inserir Objetos
];
```

### **1.3** Importar dados

> Inserir no `server.js` (`./` = Raiz do projeto)

```javascript
const dados = require("./data");
```

### **1.4** Exibir dados na rota

> Inserir no `server.js`

**Método GET**

```javascript
server.get("/pagina", function (req,res){
    return res.render("pagina",
    // Dados
    {items: dados})
}
```

**Método POST**

> Configurar formulários. `teachers.post` = dados do form

```javascript
routes.post("/", teachers.post);
```
