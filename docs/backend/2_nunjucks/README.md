# **Estrutura Backend**
> Precisa ter o node instalado.

## **1.** Configurar Template Engine

> Inserir no server.js

### **1.1** - Importar nunjucks
```javascript
const nunjucks = require("nunjucks")
```

### **1.2** - Informar engine e o tipo de arquivo do template
> O tipo do arquivo do template depende da extensão utilizada, inicialmente usamos html e depois substituimos para njk
```javascript
server.set("view engine", "njk")
```

### **1.3** - Configurar views
```javascript
nunjucks.configure("views", { express: server })
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
        {% block <!-- NOME DO BLOCO 1 --> %}{% endblock %}
    </head>
    <body>
        {% block <!-- NOME DO BLOCO 2 --> %}{% endblock %}
   </body>
</html>
```

### **2.2** - Páginas

As páginas receberam o arquivo `layout.njk` e poderão ser compostas por outros conteúdos, presentes só nelas.
> Exemplo: `sobre.njk`

```html
{% extends "layout.njk" %}

{% block <!-- NOME DO BLOCO 2 --> %}
    <section class="about">
        <img src="/images/perfil.jpg" alt="Foto Perfil">
    </section>
{% endblock %}
```
---

## **3.** Estrutura de dados



---

### **:speech_balloon:** Comandos

| **Comando**                         | **Descritivo**                  |
| ----------------------------------- | ------------------------------- |
| `{% block nome %}`                  | *Início do bloco de conteúdo*   |
| `{% endblock %}`                    | *Finaliza do bloco de conteúdo* |
| `{% extends "nome-template.njk" %}` | *Insere o conteúdo padrão*      |