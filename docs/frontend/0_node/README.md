# **Node**: Instruções

[![](https://img.shields.io/badge/1.-Dev%20Dependencies-4969D7?style=flat-square&labelColor=21275C)](#1-dependencias-desenvolvimento)

---

## **1.** Dependencias desenvolvimento

As dependências abaixo devem ser instaladas como desenvolvimento `-D`

### **1.1** - Nodemon

> Reload automático de servidor

`npm i nodemon`

```json
"scripts": {
    "nodemon": "nodemon src/server.js"
}
```

### **1.2** - Browser-sync

> Reload automático do front

`npm i browser-sync`

```json
"scripts": {
    "browsersync": "browser-sync start --proxy http://localhost:5000 --files 'public, views'"
}
```

### **1.3** - npm-run-all

> Rodar vários scripts

`npm i npm-run-all`

```json
"scripts": {
    "start": "npm-run-all -p nodemon browsersync"
}
```
