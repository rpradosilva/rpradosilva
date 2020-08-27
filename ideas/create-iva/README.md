# :bulb: **NPM** **`create-iva`** - Pacote para criar IVAs

## *Ideia*
Desenvolver um `npm` + CLI para facilitar o desenvolvimento de materiais para iPad de qualquer plataforma de CRM. (*open source - cli-scaffolding*).

## Referências
> [folder-structure-generator](https://github.com/krisalay/folder-structure-generator)

> [como criar cli](https://medium.com/henriquekuwai/criando-sua-cli-com-node-js-d6dee7d03110)

> [como criar cli - da2k](https://blog.da2k.com.br/2015/03/20/criando-uma-ferramenta-de-cli-com-nodejs/)

> [Criar CLI - Rocketseat](https://www.youtube.com/watch?v=Rt-xG_VzD6M)

> [Publicar NPM - Rocketseat](https://www.youtube.com/watch?v=OOecQMZMkqY)


## Getting Started
> Precisa do Node.

1. Instalar dependencias

`npm install`

1. Rodar projeto

`npm start`

1. Estrutura de pasta

`A Estrutura de pasta será criada na raiz.`

## Escopo
- Qual tipo de IVA?
- Título do IVA
- Quantidade de slides (nome de slides de acordo com o título) 
- Gerar estrutura de pasta

### **Veeva Folder Structure**
    .
    ├── presentation                    # Presentation
    │   ├── slide                       # Slide
    │   │   ├── index.html              # Index
    │   │   ├── thumb.png               # Thumbnail for ipad
    │   │   ├── images                  # Local images
    │   │   │   ├── conteudo.png
    │   │   │   ├── popup.png
    │   │   │   │
    .    
    ├── shared                          # Shared resources
    │   ├── js                          # Global scripts and libs
    │   │   ├── scripts.js          
    │   │   ├── routes.js               # Routes with veeva library
    │   │   ├── veeva-library.js        # Veeva library
    │   ├── css                         # Global styles
    │   │   ├── main.css
    │   ├── fonts
    │   ├── images                      # Global images
    │   │   ├── logo.png
    └──

### **IQVIA Folder Structure**
    .
    ├── presentation                        # Presentation
    │   ├── slide                           # Slide
    │   │   ├── index.html                  # Index
    │   │   ├── media                       # Images
    │   │   │   ├── images
    │   │   │   │   ├──thumbnails           # Thumbnail for ipad
    │   │   │   │   │   ├──200x150px.jpg
    │   │   │   │   conteudo.png
    │   │   ├── export                      # PDf send to e-mail
    │   │   │   ├── export.pdf
    │   │   ├── fonts
    │   │   ├── css                         # Styles
    │   │   │   ├── main.css
    │   │   ├── js                          # Scripts
    │   │   │   ├── scripts.js
    │   │   │   ├── routes.js               # Routes
    │   │   ├── parameters                  # Config
    │   │   │   ├── parameters.xml
    └──
    .

---

## ANOTAÇÕES

- formatar menu (quantos itens no menu?)
- gerar slide a partir de um slide base
- add slides a partir de uma apresentação
- fazer o zip a partir do slide