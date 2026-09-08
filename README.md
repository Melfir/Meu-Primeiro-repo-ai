Bem-vindo ao guia completo de Markdown! Se você precisa escrever documentações, criar arquivos `README.md` para seus projetos ou simplesmente formatar textos de forma rápida, você está no lugar certo.

O Markdown é uma linguagem de marcação incrivelmente simples. Em vez de usar botões para colocar o texto em negrito ou criar listas (como no Word), você usa **símbolos** diretamente no texto.

Abaixo, você encontrará **todos os principais recursos** do Markdown. Para cada recurso, vou mostrar **como você escreve** e **como ele fica** depois de renderizado.

---

## 📑 Índice
1. [Títulos (Cabeçalhos)](#1-títulos-cabeçalhos)
2. [Formatação de Texto](#2-formatação-de-texto)
3. [Listas](#3-listas)
4. [Links](#4-links)
5. [Imagens](#5-imagens)
6. [Citações (Blockquotes)](#6-citações-blockquotes)
7. [Código](#7-código)
8. [Tabelas](#8-tabelas)
9. [Linhas Horizontais](#9-linhas-horizontais)
10. [Listas de Tarefas (Checklists)](#10-listas-de-tarefas-checklists)
11. [Dicas Extras (HTML no Markdown)](#11-dicas-extras-html-no-markdown)

---

## 1. Títulos (Cabeçalhos)

Para criar títulos, usamos a cerquilha (`#`). Quanto mais cerquilhas, menor o título (vai de 1 a 6).

**Como você escreve:**
```markdown
# Título Principal (H1)
## Subtítulo (H2)
### Título Nível 3 (H3)
#### Título Nível 4 (H4)
##### Título Nível 5 (H5)
###### Título Nível 6 (H6)
```

**Como fica:**
# Título Principal (H1)
## Subtítulo (H2)
### Título Nível 3 (H3)

---

## 2. Formatação de Texto

Você pode dar destaque a palavras ou frases usando asteriscos (`*`), underlines (`_`) ou tis (`~`).

**Como você escreve:**
```markdown
Isso é um texto em **Negrito**. (ou __Negrito__)
Isso é um texto em *Itálico*. (ou _Itálico_)
Isso é um texto em ***Negrito e Itálico***.
Isso é um texto ~~Tachado / Riscado~~.
```

**Como fica:**
Isso é um texto em **Negrito**.
Isso é um texto em *Itálico*.
Isso é um texto em ***Negrito e Itálico***.
Isso é um texto ~~Tachado / Riscado~~.

---

## 3. Listas

### Listas Desordenadas (Com marcadores)
Use hífen (`-`), asterisco (`*`) ou sinal de mais (`+`).

**Como você escreve:**
```markdown
- Maçã
- Banana
  - Prata (use espaços para criar sub-listas)
  - Nanica
- Laranja
```

**Como fica:**
- Maçã
- Banana
  - Prata
  - Nanica
- Laranja

### Listas Ordenadas (Com números)
Use números seguidos de ponto.

**Como você escreve:**
```markdown
1. Acordar
2. Tomar café
3. Codar
   1. Revisar PRs
   2. Escrever testes
```

**Como fica:**
1. Acordar
2. Tomar café
3. Codar
   1. Revisar PRs
   2. Escrever testes

---

## 4. Links

Para criar um link, coloque o texto que vai aparecer entre colchetes `[]` e a URL entre parênteses `()`.

**Como você escreve:**
```markdown
[Acesse o Google aqui](https://www.google.com)
```

**Como fica:**
[Acesse o Google aqui](https://www.google.com)

---

## 5. Imagens

É quase igual aos links, mas tem um ponto de exclamação `!` no começo. O texto entre colchetes serve como "texto alternativo" (para leitores de tela ou caso a imagem falhe).

**Como você escreve:**
```markdown
![Logo do Markdown](https://markdown-here.com/img/icon256.png)
```

**Como fica:**
*(Aqui apareceria a logo do Markdown, mas como é um exemplo, imagine uma logo bem bonita!)*
![Logo do Markdown](https://markdown-here.com/img/icon256.png)

---

## 6. Citações (Blockquotes)

Usado para destacar frases ou citações de outras pessoas. Use o sinal de maior que (`>`).

**Como você escreve:**
```markdown
> "A simplicidade é o último grau de sofisticação." 
> - Leonardo da Vinci

Você pode aninhar citações também:
> Nível 1
>> Nível 2
```

**Como fica:**
> "A simplicidade é o último grau de sofisticação." 
> - Leonardo da Vinci

> Nível 1
>> Nível 2

---

## 7. Código

### Código na mesma linha (Inline)
Use crases simples (`` ` ``) para destacar pequenos trechos de código ou comandos no meio do texto.

**Como você escreve:**
```markdown
Para instalar as dependências, digite `npm install` no terminal.
```
**Como fica:**
Para instalar as dependências, digite `npm install` no terminal.

### Blocos de Código (Multi-linhas)
Use três crases (```` ``` ````) no começo e no fim. Se você colocar o nome da linguagem ao lado das primeiras crases, o código fica colorido (Syntax Highlighting).

**Como você escreve:**
````markdown
```javascript
function saudacao(nome) {
  console.log("Olá, " + nome + "!");
}
saudacao("Rhuan");
```
````

**Como fica:**
```javascript
function saudacao(nome) {
  console.log("Olá, " + nome + "!");
}
saudacao("Rhuan");
```

---

## 8. Tabelas

Use barras verticais (`|`) para separar as colunas e hifens (`-`) para criar o cabeçalho. Você pode alinhar o texto usando dois pontos (`:`).

**Como você escreve:**
```markdown
| Alinhado à Esquerda | Centralizado | Alinhado à Direita |
| :--- | :---: | ---: |
| Linha 1 | Dado A | $10 |
| Linha 2 | Dado B | $20 |
```

**Como fica:**
| Alinhado à Esquerda | Centralizado | Alinhado à Direita |
| :--- | :---: | ---: |
| Linha 1 | Dado A | $10 |
| Linha 2 | Dado B | $20 |

---

## 9. Linhas Horizontais

Para criar uma linha que separa partes do documento, use três ou mais hifens (`---`), asteriscos (`***`) ou underlines (`___`).

**Como você escreve:**
```markdown
Texto acima da linha.

---

Texto abaixo da linha.
```

**Como fica:**
Texto acima da linha.

---

Texto abaixo da linha.

---

## 10. Listas de Tarefas (Checklists)

Muito úteis no GitHub para acompanhar o progresso de algo.

**Como você escreve:**
```markdown
- [x] Tarefa concluída (coloca um 'x' no meio)
- [ ] Tarefa pendente (deixa um espaço em branco)
- [ ] Outra tarefa pendente
```

**Como fica:**
- [x] Tarefa concluída
- [ ] Tarefa pendente
- [ ] Outra tarefa pendente

---

## 11. Dicas Extras (HTML no Markdown)

Como o Markdown é convertido para HTML, você pode usar algumas tags HTML diretamente!

### ⌨️ Teclas de Atalho (`<kbd>`)
```markdown
Pressione <kbd>Ctrl</kbd> + <kbd>C</kbd> para copiar.
```
**Como fica:**
Pressione <kbd>Ctrl</kbd> + <kbd>C</kbd> para copiar.

### 🔽 Menu Retrátil (Dropdown/Details)
Excelente para esconder informações longas.
```markdown
<details>
  <summary>Clique aqui para ver o segredo</summary>
  
  Você achou a mensagem secreta! Parabéns.
</details>
```
**Como fica:**
<details>
  <summary>Clique aqui para ver o segredo</summary>
  
  Você achou a mensagem secreta! Parabéns.
</details>

---

> **Dica do Sênior:** Salve este arquivo ou mantenha ele aberto como referência. Praticar é a melhor forma de fixar o uso de todas essas formatações. Bom trabalho!
