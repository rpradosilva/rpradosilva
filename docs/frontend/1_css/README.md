# **Estrutura Frontend**: CSS
[![](https://img.shields.io/badge/1.-:root-4969D7?style=flat-square&labelColor=21275C)](#1-root)
[![](https://img.shields.io/badge/2.-Pseudo%20Elementos-4969D7?style=flat-square&labelColor=21275C)](#2-pseudo-elementos)
___

## **1.** :root
> Importante para manter a consistência da interface

> Facilita o uso do `dark mode`
```css
:root {
    --highlight: hsl(5, 80%, 92%);
    --default: hsl(0, 0%, 7%);
    --default-40: hsl(0, 0%, 40%);
    --default-60: hsl(0, 0%, 60%);
    --default-80: hsl(0, 0%, 80%);
    --default-100: hsl(0, 0%, 100%);
    --modal: #ffffff;
    --modal-overlay: rgba(0, 0, 0, .7);
    --modal-close: hsl(5, 80%, 92%);
    --modal-close-btn: hsl(5, 80%, 72%);
    --xs: 4px;
    --sm: 8px;
    --md: 16px;
    --lg: 24px;
    --xl: 36px;
    --wrapper: 940px;
}
```
---
## **2.** Pseudo Elementos
> Precisa sempre ter o parametro `content: "";`

> O elemento pai precisa sempre ter o `position: relative;`
```css
div { position: relative; }
div::after { content: ""; position: absolute; }
```