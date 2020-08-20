# :bulb: **`GAE`** - **G**erador de **A**ssinatura de **E**-mails

## *Ideia*
Desenvolver uma aplicação que gere assinaturas de e-mail responsivas para pessoas ou empresas, de forma customizável e que seja de código livre (*open source*).

## *Referências*

> [Resultados Digitais](https://resultadosdigitais.com.br/ferramentas/assinatura-de-email/cadastro)

> [Hubspot](https://br.hubspot.com/email-signature-generator)

> [Mysignature](https://pt.mysignature.io/editor)

> [Newoldstamp](https://newoldstamp.com/editor/)

> [Wisestamp](https://webapp.wisestamp.com/?_ga=2.55767586.803905847.1596758964-1697072610.1596758964)

> [htmlsig](https://htmlsig.com/#main-container)

> [Rock Content](https://rockstamp.rockcontent.com/#assinatura)

## *Projeto*

### **Público/Personas**
- Técnico TI da empresa
- Profissionais que querem deixar seu e-mail corporativo (Freelancers & funcionários)

### **Descritivo**
1. Gerar rapidamente minha assinatura de e-mail
    > Acessar o domínio, ex: `gae.github.io`

2. Informar meus dados pessoais
      > Nome (*minímo 2 letras*) :pushpin:

      > Sobrenome (*minímo 2 letras*) :pushpin:

      > Foto 

      > Telefone pessoal (*mask +55 11 00000-0000 e adicionar anchor: cel:+5511000000000*)

      > Redes Sociais (*Inserir link e ícone*)
3. Informar meus dados profissionais
      > E-mail (*@empresa.com; @empresa e . + inserir mailto no texto*) :pushpin: :office: :lock:

      > Telefone comercial (*mask +55 11 00000-0000 e adicionar anchor: cel:+5511000000000*) :pushpin: :office: :lock:
      
      > Logo Empresa (*inserir site na imagem*) :office: :lock:

      > Disclaimer :office: :lock:
4. Formatar minha assinatura
    > Cores: Primária, Secundária e de apoio (*inserir seletor de cores*) :pushpin: :office: :lock:

    > Tamanho de texto: Título, subtítulo e disclaimer :pushpin: :office: :lock:

    > 
5. Ver como ficou minha assinatura
    > A assinatura deve funcionar como um live preview (*onkeypress*)
6. Inserir no meu e-mail
    > Inserir direto no gmail (*API*)

    > `Copy to clipboard` código HTML

    > Exportar png

### **Estrutura de dados**


  - [ ] Telefone
    - [ ] Customização para empresa (*Fixo*)
    - [ ] Telefone pessoal (*+55 11 9 9999-9999*)
    - [ ] Inserir Link (*tel*)

  - [ ] Redes Sociais (*Opcional*)
    - [ ] Adicionar links
    - [ ] Customização para empresa
    - [ ] Inserir Link

- [ ] Os dados devem preencher a assinatura automáticamente (*live preview; onkeypress*)

- [ ] Copiar para área de transferência

- [ ] Exportar HTML

- [ ] Exportar para o Gmail (*API*)

### **Monetização**

- [ ] Carbon

- [ ] Google Adsense

- [ ] Donate
