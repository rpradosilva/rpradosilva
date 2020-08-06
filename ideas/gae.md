# **`GAE`** - **G**erador de **A**ssinatura de **E**-mails

## *Ideia*
Desenvolver uma aplicação que crie assinaturas de e-mail responsivas para pessoas ou empresas, de forma customizável e que seja de código livre (*open source*).

```mermaid
graph TB
A[User Data] --> B[Round edge]
    B --> C{Decision}
    C -->|One| D[Result one]
    C -->|Two| E[Result two]
```

## *Tarefas*

### Design

Utilizar as features abaixo para criar a interface.

### Gerar assinatura
- [ ] Gerar assinatura à partir de um input de dados (*form*)
- [ ] Criar e validar inputs
  - [ ] Cores
    - [ ] Destaque
    - [ ] Primária
    - [ ] Secundária
  - [ ] Tamanho de texto
  - [ ] Foto
    - [ ] Logo da empresa
    - [ ] Foto da pessoa
    - [ ] Inserir Link
  - [ ] Nome (*Mínimo 2 letras*)
  - [ ] E-mail
    - [ ] Customização para empresa (*@empresa.com; @empresa e .*)
    - [ ] Padrão (*@empresa.com; @ e .*)
    - [ ] Inserir Link (*mailto*)
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

### Monetização

- [ ] Carbon
- [ ] Google Adsense
- [ ] Donate
