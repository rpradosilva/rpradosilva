# **Estrutura Backend**: Nunjucks

[![](https://img.shields.io/badge/1.-Configurar%20Template%20Engine-4969D7?style=flat-square&labelColor=21275C)](#1-configurar-template-engine)
[![](https://img.shields.io/badge/2.-Nunjucks%20Templates-4969D7?style=flat-square&labelColor=21275C)](#2-nunjucks-templates)
[![](https://img.shields.io/badge/3.-Estrutura%20de%20dados-4969D7?style=flat-square&labelColor=21275C)](#3-estrutura-de-dados)

[![](https://img.shields.io/badge/‣%20Importante-000033?style=flat-square)](#bomb-importante)
[![](https://img.shields.io/badge/‣%20Comandos-000033?style=flat-square)](#speech_balloon-comandos)

---

## **1.** Configurar Template Engine

> Inserir no server.js

### **1.1** - Importar nunjucks

```javascript
const nunjucks = require("nunjucks");
```

### **1.2** - Informar engine e o tipo de arquivo do template

> O tipo do arquivo do template depende da extensão utilizada, inicialmente usamos html e depois substituimos para njk

```javascript
server.set("view engine", "njk");
```

### **1.3** - Configurar views

```javascript
nunjucks.configure("views", { express: server });
```

---

## **2.** Nunjucks Templates

> Necessário identificar elementos que aparecem em todas as páginas e os que são exclusivos de cada página

### **2.1** - Criar estrutura padrão

Crie o arquivo `layout.njk` na pasta views, com os elementos/tags que se repetem em toda estrutura do projeto.

> Tudo que irá se **repetir** deve **ficar fora** dos blocos

```html
<html>
  <head>
    {% block
    <!-- NOME DO BLOCO 1 -->
    %}{% endblock %}
  </head>
  <body>
    {% block
    <!-- NOME DO BLOCO 2 -->
    %}{% endblock %}
  </body>
</html>
```

### **2.2** - Páginas

As páginas receberam o arquivo `layout.njk` e poderão ser compostas por outros conteúdos, presentes só nelas.

> Exemplo: `sobre.njk`

```html
{% extends "layout.njk" %} {% block
<!-- NOME DO BLOCO 2 -->
%}
<section class="about">
  <img src="/images/perfil.jpg" alt="Foto Perfil" />
</section>
{% endblock %}
```

---

## **3.** Estrutura de dados

### **3.1** Carregar dados

> Com a variável definida no serivdor, usar estrutura de repetição

```html
{% for item in items %}

<!-- Estrura do item aqui -->
<div>{{item.id}}</div>

{% endfor %}
```

### **3.2** Condicional

> If e Else

```
{% if item.buy %}
    ACESSAR
{% else %}
    COMPRAR
{% endif %}
```

---

## :bomb: Importante

### Inserir Tags HTML

> No Array:

```javascript
const array = [
  {
    // Usar aspas simples
    logo: '<img src="/images/perfil.jpg" alt="Foto Perfil">',
  },
];
```

> No `server.js`, inserir o autoescape:

```javascript
nunjucks.configure("views", {
  autoescape: false,
});
```

### Remover Cache

> No `server.js`, inserir:

```javascript
nunjucks.configure("views", {
  noCache: true,
});
```

---

## **:speech_balloon:** Comandos

| **Comando**                                   | **Descritivo**                        |
| --------------------------------------------- | ------------------------------------- |
| `{% block nome %}` & `{% endblock %}`         | _Bloco de conteúdo_                   |
| `{% extends "nome-template.njk" %}`           | _Insere o conteúdo padrão (Template)_ |
| `{% for item in items %}` & `{% endfor %}`    | _Estrutura de repetição_              |
| `{% if nome %}`, `{% else %}` & `{% endif %}` | _Condicionais_                        |
