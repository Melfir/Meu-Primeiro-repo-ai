Bem-vindo ao guia de referência rápida para Python! Este documento foi criado para ser o seu "Cheat Sheet" (Guia de Bolso) no dia a dia. Aqui você encontrará os comandos, estruturas e funções mais essenciais da linguagem.

---

## 📑 Índice
1. [Variáveis e Tipos de Dados Básicos](#1-variáveis-e-tipos-de-dados-básicos)
2. [Operadores Matemáticos e Lógicos](#2-operadores-matemáticos-e-lógicos)
3. [Estruturas de Condição (If / Else)](#3-estruturas-de-condição)
4. [Estruturas de Repetição (Loops)](#4-estruturas-de-repetição)
5. [Estruturas de Dados (Listas, Tuplas, Dicionários, Sets)](#5-estruturas-de-dados)
6. [Compreensão de Listas (List Comprehension)](#6-compreensão-de-listas)
7. [Funções e Lambdas](#7-funções-e-lambdas)
8. [Manipulação de Arquivos](#8-manipulação-de-arquivos)
9. [Tratamento de Exceções (Erros)](#9-tratamento-de-exceções)
10. [Funções Integradas Úteis](#10-funções-integradas-úteis)
11. [Comandos Úteis de Terminal (Pip e Venv)](#11-comandos-úteis-de-terminal)
12. [Armadilhas Comuns em Python](#12-armadilhas-comuns-em-python)

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

# Conversão de tipos
numero_str = "42"
numero_int = int(numero_str)      # Converte para inteiro
numero_float = float(numero_str)  # Converte para float
texto = str(100)                  # Converte para string
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

# Comparação
print(10 == 10)  # True (igualdade)
print(10 != 5)   # True (diferença)
print(10 > 5)    # True (maior que)
print(10 < 5)    # False (menor que)
print(10 >= 10)  # True (maior ou igual)
print(10 <= 5)   # False (menor ou igual)
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

# Múltiplas condições
idade = 20
tem_carteira = True

if idade >= 18 and tem_carteira:
    print("Pode dirigir!")
elif idade >= 18 and not tem_carteira:
    print("Maior de idade, mas sem carteira")
else:
    print("Menor de idade")

# Verificar se um valor está em uma lista/sequência
linguagens = ["Python", "JavaScript", "Java"]
if "Python" in linguagens:
    print("Python está na lista!")
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

# Loop reverso
for i in range(5, 0, -1):
    print(i)  # Imprime: 5, 4, 3, 2, 1

# Usando break e continue
for i in range(10):
    if i == 3:
        continue  # Pula para a próxima iteração
    if i == 7:
        break     # Sai do loop completamente
    print(i)
```

### `while` (Enquanto uma condição for verdadeira)
```python
contador = 0
while contador < 5:
    print(contador)
    contador += 1 # Não esqueça de incrementar para não gerar um loop infinito!

# Usando break e continue
while True:
    entrada = input("Digite 'sair' para saír: ")
    if entrada.lower() == "sair":
        break
    print(f"Você digitou: {entrada}")
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

# Slicing (fatiamento)
numeros = [0, 1, 2, 3, 4, 5]
print(numeros[1:4])     # [1, 2, 3] - do índice 1 ao 3
print(numeros[:3])      # [0, 1, 2] - primeiros 3 elementos
print(numeros[2:])      # [2, 3, 4, 5] - do índice 2 até o final
print(numeros[::-1])    # [5, 4, 3, 2, 1, 0] - reverso
print(numeros[::2])     # [0, 2, 4] - a cada 2 elementos
```

### Tuplas (Imutáveis, ordenadas)
```python
coordenadas = (10.5, 20.3)
print(coordenadas[0])   # Acessa o primeiro elemento: 10.5
# coordenadas[0] = 15.0  <-- Isso geraria um erro, pois tuplas não mudam.

# Desempacotamento
x, y = coordenadas
print(x, y)  # 10.5 20.3
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
del usuario["linguagem"]        # Remove uma chave

# Verificar se uma chave existe
if "nome" in usuario:
    print(f"Olá, {usuario['nome']}")

# Iterando sobre dicionários
for chave, valor in usuario.items():
    print(f"{chave}: {valor}")

# Apenas chaves ou valores
chaves = usuario.keys()
valores = usuario.values()

# Obter valor com valor padrão se chave não existir
telefone = usuario.get("telefone", "Não informado")
```

### Sets (Conjuntos: sem repetição, não ordenados)
```python
numeros_unicos = {1, 2, 2, 3, 4, 4}
print(numeros_unicos)  # Saída: {1, 2, 3, 4}

# Operações de conjunto
conjunto_a = {1, 2, 3}
conjunto_b = {3, 4, 5}

print(conjunto_a | conjunto_b)  # União: {1, 2, 3, 4, 5}
print(conjunto_a & conjunto_b)  # Interseção: {3}
print(conjunto_a - conjunto_b)  # Diferença: {1, 2}

# Adicionar e remover
numeros_unicos.add(5)
numeros_unicos.remove(2)
```

---

## 6. Compreensão de Listas

Uma forma concisa e elegante de criar listas (muito comum em Python).

```python
# Criar uma lista de quadrados (0 a 9)
quadrados = [x**2 for x in range(10)]

# Filtrar apenas os números pares
pares = [x for x in range(10) if x % 2 == 0]

# Transformar e filtrar simultaneamente
nomes = ["alice", "bob", "carlos"]
nomes_maiusculos = [nome.upper() for nome in nomes if len(nome) > 3]

# Compreensão de dicionários
numeros = [1, 2, 3, 4, 5]
dict_quadrados = {num: num**2 for num in numeros}
# Resultado: {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

---

## 7. Funções e Lambdas

Blocos de código reutilizáveis.

```python
# Função básica com argumentos padrão
def saudacao(nome, saudacao="Olá"):
    """Função que retorna uma saudação personalizada."""
    return f"{saudacao}, {nome}!"

print(saudacao("Rhuan"))           # Olá, Rhuan!
print(saudacao("Rhuan", "Bom dia")) # Bom dia, Rhuan!

# Função com *args (número variável de argumentos)
def somar(*numeros):
    total = 0
    for num in numeros:
        total += num
    return total

print(somar(1, 2, 3, 4, 5))  # 15

# Função com **kwargs (argumentos nomeados variáveis)
def criar_perfil(nome, **dados):
    perfil = {"nome": nome}
    perfil.update(dados)
    return perfil

perfil = criar_perfil("João", idade=30, cidade="São Paulo", profissao="Dev")
print(perfil)
# {'nome': 'João', 'idade': 30, 'cidade': 'São Paulo', 'profissao': 'Dev'}

# Lambda (Funções anônimas de uma linha)
dobro = lambda x: x * 2
print(dobro(5))  # Saída: 10

# Lambdas com múltiplos parâmetros
soma_lambda = lambda x, y: x + y
print(soma_lambda(3, 7))  # 10

# Type hints (dicas de tipo)
def multiplicar(a: int, b: int) -> int:
    """Multiplica dois números inteiros e retorna um inteiro."""
    return a * b

resultado: int = multiplicar(5, 3)
```

---

## 8. Manipulação de Arquivos

Sempre use o bloco `with` para garantir que o arquivo será fechado corretamente.

```python
# Escrevendo em um arquivo ('w' para sobrescrever, 'a' para adicionar)
with open("meu_arquivo.txt", "w", encoding="utf-8") as arquivo:
    arquivo.write("Olá, este é um arquivo de texto!\n")
    arquivo.write("Segunda linha\n")

# Lendo um arquivo inteiro ('r')
with open("meu_arquivo.txt", "r", encoding="utf-8") as arquivo:
    conteudo = arquivo.read()
    print(conteudo)

# Lendo linha por linha
with open("meu_arquivo.txt", "r", encoding="utf-8") as arquivo:
    for linha in arquivo:
        print(linha.strip())  # .strip() remove quebras de linha

# Lendo todas as linhas em uma lista
with open("meu_arquivo.txt", "r", encoding="utf-8") as arquivo:
    linhas = arquivo.readlines()

# Adicionando conteúdo (append)
with open("meu_arquivo.txt", "a", encoding="utf-8") as arquivo:
    arquivo.write("Nova linha adicionada!\n")
```

---

## 9. Tratamento de Exceções

Para evitar que seu programa quebre quando ocorrer um erro inesperado.

```python
# Tratamento básico
try:
    resultado = 10 / 0
except ZeroDivisionError:
    print("Erro: Não é possível dividir por zero!")
except Exception as e:
    print(f"Ocorreu um erro genérico: {e}")
finally:
    print("Isso sempre será executado (com ou sem erro).")

# Tratamento com else (executa se NÃO houver exceção)
try:
    numero = int(input("Digite um número: "))
    resultado = 100 / numero
except ValueError:
    print("Erro: Digite um número válido!")
except ZeroDivisionError:
    print("Erro: Não pode dividir por zero!")
else:
    print(f"Resultado: {resultado}")
finally:
    print("Operação finalizada.")

# Levantando exceções personalizadas
def validar_idade(idade):
    if idade < 0:
        raise ValueError("A idade não pode ser negativa!")
    if idade > 150:
        raise ValueError("A idade parece inválida!")
    return True

try:
    validar_idade(-5)
except ValueError as erro:
    print(f"Erro de validação: {erro}")

# Exceção personalizada
class ErroPersonalizado(Exception):
    pass

try:
    raise ErroPersonalizado("Este é um erro customizado!")
except ErroPersonalizado as e:
    print(f"Capturei meu erro: {e}")
```

---

## 10. Funções Integradas Úteis

```python
# map() - Aplica uma função a cada elemento
numeros = [1, 2, 3, 4, 5]
dobrados = list(map(lambda x: x * 2, numeros))
print(dobrados)  # [2, 4, 6, 8, 10]

# filter() - Filtra elementos baseado em condição
pares = list(filter(lambda x: x % 2 == 0, numeros))
print(pares)  # [2, 4]

# zip() - Combina múltiplas sequências
nomes = ["Alice", "Bob", "Carlos"]
idades = [25, 30, 28]
pessoas = list(zip(nomes, idades))
print(pessoas)  # [('Alice', 25), ('Bob', 30), ('Carlos', 28)]

# len() - Comprimento
print(len([1, 2, 3]))      # 3
print(len("Python"))       # 6

# sorted() - Ordena
numeros = [3, 1, 4, 1, 5, 9]
ordenados = sorted(numeros)
print(ordenados)  # [1, 1, 3, 4, 5, 9]

# reversed() - Reverte
print(list(reversed([1, 2, 3])))  # [3, 2, 1]

# sum(), min(), max()
print(sum([1, 2, 3, 4, 5]))    # 15
print(min([3, 1, 4]))          # 1
print(max([3, 1, 4]))          # 4

# all() - Retorna True se todos são verdadeiros
print(all([True, True, True]))   # True
print(all([True, False, True]))  # False

# any() - Retorna True se algum é verdadeiro
print(any([False, False, True])) # True
```

---

## 11. Comandos Úteis de Terminal

Embora não sejam código Python diretamente, são essenciais para gerenciar projetos.

```bash
# Verificar a versão do Python instalada
python --version

# Executar um arquivo Python
python nome_arquivo.py

# Criar um ambiente virtual (isola as bibliotecas do projeto)
python -m venv venv

# Ativar o ambiente virtual (Windows)
venv\Scripts\activate

# Ativar o ambiente virtual (Linux/Mac)
source venv/bin/activate

# Desativar o ambiente virtual
deactivate

# Instalar um pacote/biblioteca
pip install requests

# Instalar uma versão específica
pip install requests==2.28.0

# Salvar as dependências do projeto em um arquivo
pip freeze > requirements.txt

# Instalar dependências a partir de um arquivo
pip install -r requirements.txt

# Listar pacotes instalados
pip list

# Desinstalar um pacote
pip uninstall requests
```

---

## 12. Armadilhas Comuns em Python

### 1. Argumentos padrão mutáveis
```python
# ❌ ERRADO - lista padrão é compartilhada entre chamadas
def adicionar_item(item, lista=[]):
    lista.append(item)
    return lista

print(adicionar_item(1))  # [1]
print(adicionar_item(2))  # [1, 2] - lista mantém os itens anteriores!

# ✅ CORRETO - usar None e criar nova lista
def adicionar_item(item, lista=None):
    if lista is None:
        lista = []
    lista.append(item)
    return lista

print(adicionar_item(1))  # [1]
print(adicionar_item(2))  # [2]
```

### 2. Diferença entre `is` e `==`
```python
# `==` compara valor, `is` compara identidade (referência na memória)
a = [1, 2, 3]
b = [1, 2, 3]
c = a

print(a == b)   # True (mesmos valores)
print(a is b)   # False (objetos diferentes na memória)
print(a is c)   # True (mesma referência)

# Use `is` apenas para None, True, False
if valor is None:
    print("É None")
```

### 3. Copiar listas
```python
# ❌ ERRADO - ambas apontam para a mesma lista
lista_original = [1, 2, 3]
lista_copia = lista_original
lista_copia.append(4)
print(lista_original)  # [1, 2, 3, 4] - foi modificada!

# ✅ CORRETO - criar uma cópia verdadeira
lista_copia = lista_original.copy()
lista_copia.append(4)
print(lista_original)  # [1, 2, 3] - inalterada
```

### 4. Modificar dicionário enquanto itera
```python
# ❌ ERRADO - pode causar erro
d = {"a": 1, "b": 2, "c": 3}
for chave in d:
    if chave == "b":
        del d[chave]  # RuntimeError!

# ✅ CORRETO - iterar sobre uma cópia das chaves
d = {"a": 1, "b": 2, "c": 3}
for chave in list(d.keys()):
    if chave == "b":
        del d[chave]
```

### 5. Escopo de variáveis
```python
x = "global"

def funcao():
    x = "local"  # Cria uma variável local
    print(x)     # local

print(x)  # global

# Para usar variável global dentro da função
contador = 0

def incrementar():
    global contador
    contador += 1

incrementar()
print(contador)  # 1
```

---

> **Dica Sênior:** Python é muito legível. Procure sempre escrever códigos que expliquem a si mesmos, dando bons nomes às variáveis e funções. Siga as convenções da comunidade consultando a [Documentação Oficial (PEP 8)](https://www.python.org/dev/peps/pep-0008/). Código limpo hoje = menos manutenção amanhã! 🚀
