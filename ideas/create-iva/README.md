# :bulb: **NPM** **`create-iva`** - Pacote para criar IVAs

## *Ideia*
Desenvolver um `npm` para facilitar o desenvolvimento de materiais para iPad de qualquer plataforma de CRM. (*open source*).

## Referências
> [folder-structure-generator](https://github.com/krisalay/folder-structure-generator)

## Escopo
- Qual tipo de IVA?
- Título do IVA
- Quantidade de slides (nome de slides de acordo com o título) 
- Gerar estrutura de pasta

### Veeva
- /slide_iva
  - thumb.png
  - /images
    - conteudo.png
  - index.html
    - snippet de código
    - preencher title com nome do IVA
    - linkar arquivos do shared
- /shared
  - /js
    - scripts.js
    - routes.js
      - snippet de código
      - nome de cada pasta
    - veeva-library.js
  - /css
    - main.css
      - snippet de código
  - /images
  - /fonts

### IQVIA
- /slide_iva
  - index.html
    - snippet de código
    - preencher title com nome do IVA
  - /media
    - /images
      - bg.png
      - /thumbnails
        - 200x150.jpg
  - /export
    - export.pdf
  - /fonts
  - /css
    - main.css
      - snippet de código
  - /js
    - scripts.js
    - routes.js
      - snippet de código
      - nome de cada pasta
  - /parameters
    - parameters.xml