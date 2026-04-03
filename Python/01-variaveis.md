# Variáveis em Python

## O que são
Variáveis são espaços na memória do computador
usados para guardar valores.
Pensa como uma caixa com um nome e um conteúdo dentro.

---

## Como declarar
Em Python não precisas de nenhuma keyword especial.
Simplesmente escreves o nome, o sinal de igual e o valor.
```python
nome = "Maria Wilson"
idade = 20
altura = 1.75
ativo = True
```

Diferente de outras linguagens:
```
JavaScript → let nome = "valor"
C          → char nome[] = "valor"
Python     → nome = "valor"
```

Python é a mais simples — sem keyword, sem tipo explícito.

---

## Tipos de dados básicos

### Inteiro (int)
É um número sem casas decimais.
Pode ser positivo, negativo ou zero.
Usado para contar, indexar ou representar quantidades exatas.
```python
idade = 20
ano = 2025
temperatura = -5
vidas = 3
```

---

### Float ou Real (float)
É um número com casas decimais.
Usado quando precisas de precisão — preços, medidas, notas.
O separador decimal em Python é o ponto, não a vírgula.
```python
altura = 1.75
nota = 9.5
preco = 49.99
temperatura = -3.8
```

---

### String ou Caractere (str)
É texto — qualquer sequência de letras, números ou símbolos.
Sempre entre aspas simples ou duplas.
Mesmo que o conteúdo seja um número, se estiver
entre aspas é string — não dá para calcular.
```python
nome = "Maria Wilson"
mensagem = 'Olá, mundo!'
telefone = "845123456"   # número mas é texto
vazio = ""               # string vazia também é válida
```

---

### Lógico ou Booleano (bool)
Só tem dois valores possíveis — True ou False.
Usado para tomar decisões no código.
Em Python começa sempre com letra maiúscula.
```python
logado = True
tem_permissao = False
maior_de_idade = True
conta_ativa = False
```

Atenção — diferente de outras linguagens:
```
JavaScript → true / false    (minúscula)
C          → 1 / 0           (números)
Python     → True / False    (maiúscula)
```

Se escreveres true com minúscula o Python não reconhece
e dá erro — é um dos erros mais comuns de quem vem
do JavaScript.
```python
logado = True    # correto ✅
logado = true    # erro ❌ — NameError
```

---

---

## Regras para nomear variáveis

**Pode começar com letra ou underscore — nunca com número:**
```python
nome = "Maria Wilson"     # correto ✅
_valor = 10               # correto ✅
1nome = "erro"            # errado ❌
```

**Sem espaços — usa snake_case:**
Em Python as palavras são separadas por underscore ( _ )
```python
nome_completo = "Maria Wilson"    # correto ✅
nome completo = "Maria Wilson"    # errado ❌
```

**snake_case — como funciona:**
Diferente do JavaScript que usa camelCase,
Python usa snake_case.
Todas as letras são minúsculas e
as palavras são separadas por underscore.
```python
# JavaScript usa camelCase
nomeCompleto = "Maria Wilson"

# Python usa snake_case
nome_completo = "Maria Wilson"

# Mais exemplos
idade_do_usuario = 20
cor_favorita = "verde"
total_de_pontos = 100
```

**Sensível a maiúsculas:**
nome, Nome e NOME são três variáveis diferentes.
```python
nome = "Maria Wilson"
Nome = "outro valor"   # variável diferente
```

**Apenas letras, números e underscore:**
```python
nome_1 = "válido"       # correto ✅
nome-completo = ""      # errado ❌
nome@usuario = ""       # errado ❌
```

---

## Boas práticas

**Usa nomes descritivos:**
```python
# Mau
x = 20
n = "Maria Wilson"

# Bom
idade_usuario = 20
nome_usuario = "Maria Wilson"
```

**Evita abreviações:**
```python
# Mau
usr = "Maria Wilson"

# Bom
utilizador = "Maria Wilson"
```

**Uma variável, uma responsabilidade:**
```python
# Mau
dados = "Maria Wilson 20 Moçambique"

# Bom
nome = "Maria Wilson"
idade = 20
pais = "Moçambique"
```

**Sê consistente — português ou inglês, nunca os dois:**
```python
# Misturado — evitar
user_nome = "Maria Wilson"

# Consistente em português
nome_usuario = "Maria Wilson"
idade_usuario = 20

# Consistente em inglês
username = "Maria Wilson"
user_age = 20
```

---

## Erros comuns
```python
# Começar com número
1nome = "erro"          # errado ❌

# Usar espaço
nome completo = ""      # errado ❌

# Booleano com minúscula
ativo = true            # errado ❌

# Símbolo no nome
nome-completo = ""      # errado ❌

# Misturar português e inglês
user_nome = "valor"     # evitar ❌
```