# Convenções de Projeto HTML & CSS

Este documento define as principais convenções de codificação para projetos utilizando HTML e CSS padrão.

---

## Estrutura de Pastas

```
/projeto
  /assets
    /css
    /img
    /fonts
    /js
  index.html
```

---

## HTML

### 1. Organização

- Use indentação de **2 espaços** (não use tabs).
- Utilize **letras minúsculas** para nomes de tags e atributos.
- Sempre feche as tags.
- Use a estrutura básica:

```html
<!DOCTYPE html>
<html lang="pt-br">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Título da Página</title>
    <link rel="stylesheet" href="assets/css/style.css" />
  </head>
  <body>
    <!-- Conteúdo -->
  </body>
</html>
```

### 2. Nomenclatura de Classes e IDs

- Use nomes **semânticos**.  
  Exemplo: `.menu-principal`, `#rodape`
- Separe palavras com **hífen** (`-`).
- Prefira classes a IDs para estilização.

### 3. Comentários

- Utilize comentários para seções importantes:
  ```html
  <!-- Início Menu Principal -->
  <!-- Fim Menu Principal -->
  ```

---

## CSS

### 1. Organização

- Mantenha todo CSS em arquivos dentro de `/assets/css`.
- Use um arquivo principal: `style.css`.
- Use **import** apenas em arquivos auxiliares, evite excesso.

### 2. Sintaxe

- Indente com **2 espaços**.
- Use **letras minúsculas** para propriedades e valores.
- Termine cada declaração com **ponto e vírgula**.

```css
.menu-principal {
  background-color: #fff;
  color: #333;
  padding: 16px 24px;
}
```

### 3. Nomenclatura

- Siga o padrão [BEM (Block Element Modifier)](http://getbem.com/) se necessário:
  - `.bloco`
  - `.bloco__elemento`
  - `.bloco--modificador`

- Para projetos simples, use nomes descritivos com hífen:
  - `.botao-primario`
  - `.card-produto`

### 4. Comentários

```css
/* ======== Menu Principal ======== */
/* Botões */
```

### 5. Cores e Unidades

- Use **hexadecimal** ou **rgb/rgba** para cores.
- Prefira **rem** ou **em** para tamanhos de fonte, **px** para espaçamentos.

### 6. Boas Práticas

- Evite o uso excessivo de `!important`.
- Agrupe seletores relacionados.
- Utilize reset ou normalize.css no início do projeto.

---

## Exemplo de Estrutura HTML + CSS

```html
<nav class="menu-principal">
  <ul class="menu-principal__lista">
    <li class="menu-principal__item"><a href="#">Início</a></li>
    <li class="menu-principal__item"><a href="#">Sobre</a></li>
  </ul>
</nav>
```

```css
.menu-principal {
  background: #20232a;
  padding: 1rem 2rem;
}

.menu-principal__item a {
  color: #61dafb;
  text-decoration: none;
  padding: 0.5rem 1rem;
}
```

---

## Referências

- [HTML Living Standard](https://html.spec.whatwg.org/)
- [Guia BEM](https://getbem.com/naming/)
- [MDN HTML](https://developer.mozilla.org/pt-BR/docs/Web/HTML)
- [MDN CSS](https://developer.mozilla.org/pt-BR/docs/Web/CSS)