Bem-vindo ao guia de referência rápida para Python! Este documento foi criado para ser o seu "Cheat Sheet" (Guia de Bolso) no dia a dia. Aqui você encontrará os comandos, estruturas e funções mais práticos e utilizados na linguagem Python.

---

## 📑 Índice
1. [Variáveis e Tipos de Dados Básicos](#1-variáveis-e-tipos-de-dados-básicos)
2. [Operadores Matemáticos e Lógicos](#2-operadores-matemáticos-e-lógicos)
3. [Estruturas de Condição (If / Else)](#3-estruturas-de-condição)
4. [Estruturas de Repetição (Loops)](#4-estruturas-de-repetição)
5. [Estruturas de Dados (Listas, Tuplas, Dicionários, Sets)](#5-estruturas-de-dados)
6. [Compreensão de Listas (List Comprehension)](#6-compreensão-de-listas)
7. [Funções e Lambdas](#7-funções)
8. [Manipulação de Arquivos](#8-manipulação-de-arquivos)
9. [Tratamento de Exceções (Erros)](#9-tratamento-de-exceções)
10. [Comandos Úteis de Terminal (Pip e Venv)](#10-comandos-úteis-de-terminal)

---

## 1. Variáveis e Tipos de Dados Básicos

Em Python, você não precisa declarar o tipo da variável, a linguagem identifica automaticamente.

```python
# Strings (Textos)
nome = "Rhuan"
mensagem = f"Olá, {nome}!"  # F-string (interpolação moderna)

# Integers (Números Inteiros)
idade = 25

# Floats (Números Decimais)
altura = 1.75

# Booleans (Verdadeiro ou Falso)
is_dev = True

# Descobrindo o tipo de uma variável
print(type(nome))  # Saída: <class 'str'>
```

---

## 2. Operadores Matemáticos e Lógicos

```python
# Matemáticos
soma = 10 + 5
subtracao = 10 - 5
multiplicacao = 10 * 5
divisao = 10 / 5        # Retorna float (2.0)
divisao_inteira = 10 // 3 # Retorna int (3)
resto = 10 % 3          # Retorna o resto (1)
potencia = 2 ** 3       # 2 elevado a 3 (8)

# Lógicos (AND, OR, NOT)
a = True
b = False
print(a and b)  # False (E)
print(a or b)   # True  (OU)
print(not a)    # False (NÃO)
```

---

## 3. Estruturas de Condição

Usadas para tomar decisões no código.

```python
nota = 85

if nota >= 90:
    print("Excelente!")
elif nota >= 70:
    print("Aprovado!")
else:
    print("Reprovado!")
    
# Operador Ternário (If em uma linha)
status = "Aprovado" if nota >= 70 else "Reprovado"
```

---

## 4. Estruturas de Repetição

### `for` (Para um número conhecido de iterações)
```python
# Loop em uma faixa de números (0 a 4)
for i in range(5):
    print(i)

# Loop em uma lista
frutas = ["maçã", "banana", "uva"]
for fruta in frutas:
    print(fruta)
    
# Loop com índice (enumerate)
for index, fruta in enumerate(frutas):
    print(f"{index}: {fruta}")
```

### `while` (Enquanto uma condição for verdadeira)
```python
contador = 0
while contador < 5:
    print(contador)
    contador += 1 # Não esqueça de incrementar para não gerar um loop infinito!
```

---

## 5. Estruturas de Dados

### Listas (Mutáveis, ordenadas)
```python
lista = [1, 2, 3, "Python"]
lista.append(4)         # Adiciona ao final
lista.insert(0, "A")    # Insere "A" na posição 0
lista.pop()             # Remove e retorna o último elemento
lista.remove(2)         # Remove a primeira ocorrência do valor 2
```

### Tuplas (Imutáveis, ordenadas)
```python
coordenadas = (10.5, 20.3)
# coordenadas[0] = 15.0  <-- Isso geraria um erro, pois tuplas não mudam.
```

### Dicionários (Chave-Valor)
```python
usuario = {
    "nome": "Rhuan",
    "idade": 25,
    "linguagem": "Python"
}
print(usuario["nome"])          # Acessa o valor
usuario["cidade"] = "São Paulo" # Adiciona nova chave-valor

# Iterando sobre dicionários
for chave, valor in usuario.items():
    print(f"{chave}: {valor}")
```

### Sets (Conjuntos: sem repetição, não ordenados)
```python
numeros_unicos = {1, 2, 2, 3, 4, 4}
print(numeros_unicos)  # Saída: {1, 2, 3, 4}
```

---

## 6. Compreensão de Listas

Uma forma concisa de criar listas (muito comum em Python).

```python
# Criar uma lista de quadrados (0 a 9)
quadrados = [x**2 for x in range(10)]

# Filtrar apenas os números pares
pares = [x for x in range(10) if x % 2 == 0]
```

---

## 7. Funções

Blocos de código reutilizáveis.

```python
def saudacao(nome, saudacao="Olá"):
    return f"{saudacao}, {nome}!"

print(saudacao("Rhuan"))           # Olá, Rhuan!
print(saudacao("Rhuan", "Bom dia")) # Bom dia, Rhuan!

# Lambda (Funções anônimas de uma linha)
dobro = lambda x: x * 2
print(dobro(5))  # Saída: 10
```

---

## 8. Manipulação de Arquivos

Sempre use o bloco `with` para garantir que o arquivo será fechado corretamente.

```python
# Escrevendo em um arquivo ('w' para sobrescrever, 'a' para adicionar)
with open("meu_arquivo.txt", "w", encoding="utf-8") as arquivo:
    arquivo.write("Olá, este é um arquivo de texto!
")

# Lendo um arquivo ('r')
with open("meu_arquivo.txt", "r", encoding="utf-8") as arquivo:
    conteudo = arquivo.read()
    print(conteudo)
```

---

## 9. Tratamento de Exceções

Para evitar que seu programa quebre quando ocorrer um erro inesperado.

```python
try:
    resultado = 10 / 0
except ZeroDivisionError:
    print("Erro: Não é possível dividir por zero!")
except Exception as e:
    print(f"Ocorreu um erro genérico: {e}")
finally:
    print("Isso sempre será executado (com ou sem erro).")
```

---

## 10. Comandos Úteis de Terminal

Embora não sejam código Python diretamente, são essenciais para gerenciar projetos.

```bash
# Verificar a versão do Python instalada
python --version

# Criar um ambiente virtual (isola as bibliotecas do projeto)
python -m venv venv

# Ativar o ambiente virtual (Windows)
venv\Scripts\activate
# Ativar o ambiente virtual (Linux/Mac)
source venv/bin/activate

# Instalar um pacote/biblioteca
pip install requests

# Salvar as dependências do projeto em um arquivo
pip freeze > requirements.txt

# Instalar dependências a partir de um arquivo
pip install -r requirements.txt
```

---
> **Dica Sênior:** Python é muito legível. Procure sempre escrever códigos que expliquem a si mesmos, dando bons nomes às variáveis e funções. Consulte a [Documentação Oficial (PEP 8)](https://peps.python.org/pep-0008/) para ver as boas práticas de estilo!
