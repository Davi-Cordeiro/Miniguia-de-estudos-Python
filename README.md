
# 🐍 Guia de Estudos Python: Do Zero ao Avançado

Este guia de estudos foi desenvolvido para orientar sua jornada no aprendizado da linguagem Python, cobrindo desde a configuração do ambiente até estruturas de dados avançadas e boas práticas de desenvolvimento.

---

## 📌 Visão Geral e Mercado

- O mercado de tecnologia exige cada vez mais profissionais que saibam programar e dominem a lógica de software.
- Python é uma linguagem de alto nível, interpretada, de propósito geral e de código aberto (*Open-Source*), criada por Guido van Rossum em 1991.
- Ela se destaca no mercado por sua sintaxe clara, excelente legibilidade, grande comunidade global e suporte multiplataforma (Windows, macOS, Linux).
- Suas áreas de aplicação englobam Desenvolvimento Web, Análise de Dados, Inteligência Artificial, Automação de Scripts, Aplicativos Desktop, Dispositivos Móveis, Internet das Coisas (IoT) e Jogos.
- Não é necessário ter inglês avançado ou ser especialista em matemática para aprender a programar.
- O aprendizado da programação desenvolve o raciocínio lógico, a criatividade e a capacidade de resolução de problemas.

---

## 🛠️ Módulo 0: Fundamentos e Configuração de Ambiente

- **Funcionamento do Python**: O código-fonte em Python é traduzido em *Bytecode* e executado pela *Python Virtual Machine* (PVM), que converte as instruções em código de máquina para o computador.
- **Instalação do Python**: Baixado no site oficial `python.org`. Durante o processo no Windows, é fundamental marcar a caixa **"Add Python to PATH"** para que o sistema operacional reconheça o executável.
- **Configuração do VS Code**: Instalação do editor Visual Studio Code acompanhado da extensão oficial do Python desenvolvida pela Microsoft.
- **Ajustes Recomendados**:
  - Ativar o *Auto Save* (`File > Auto Save`) para salvar arquivos automaticamente.
  - Habilitar o *Word Wrap* (`settings > word wrap`) para evitar barras de rolagem horizontais.
  - Formatar o código seguindo o guia de estilo PEP 8.

---

## 🚀 Módulo 1: Primeiros Passos e Sintaxe Básica

- **Comentários**: Linha única usando `#`, múltiplas linhas ou inline. O interpretador ignora comentários, servindo para documentação.
- **Saída de Dados (`print()`)**: Exibe mensagens no terminal. Suporta aspas simples ou duplas.
  - **Caracteres de Escape**: `\n` (quebra de linha), `\t` (tabulação), `\\` (barra invertida) e `\"` (aspas no texto).
- **Entrada de Dados (`input()`)**: Solicita informações do usuário. Retorna os dados digitados sempre no formato de texto (*string*).
- **Tipos de Dados Primitivos**:
  - `int`: Números inteiros.
  - `float`: Números decimais/ponto flutuante.
  - `str`: Textos e sequências de caracteres entre aspas.
  - `bool`: Valores lógicos `True` ou `False`.
  - `NoneType` (`None`): Representa a ausência de valor ou tipo não definido.

```python
# Exemplo de entrada e saída com tipos primitivos
nome = input("Digite seu nome: ")
idade = int(input("Digite sua idade: "))
altura = float(input("Digite sua altura: "))
print(f"Olá {nome}, você tem {idade} anos e {altura}m de altura.")
```

---

## 📐 Módulo 2: Operadores e Manipulação de Dados

- **Operadores Aritméticos**:
  - Adição (`+`), Subtração (`-`), Multiplicação (`*`), Divisão (`/`).
  - Divisão inteira (`//`), Resto da divisão/Módulo (`%`), Potenciação (`**`).
- **Operadores de Atribuição Simplificados**: `+=`, `-=`, `*=`, `/=`.
- **Manipulação de Strings**:
  - Indexação positiva (iniciando em `0`) e negativa (iniciando em `-1`). Fatiamento (*slicing*) com a sintaxe `[início:fim:passo]`.
  - Métodos fundamentais: `strip()` (remove espaços nas pontas), `lower()` / `upper()` (altera a caixa), `replace()` (substitui caracteres), `split()` (divide string em lista), `find()` (localiza índice), `count()` (conta ocorrências).
  - **f-strings**: Sintaxe `f"Texto {variavel}"` para intercalar variáveis diretamente em textos.
- **Operações Numéricas e Arredondamento**:
  - `abs()`: Retorna o valor absoluto.
  - `round()`: Arredonda números decimais.
  - Módulo `math`: `math.floor()` (arredonda para baixo), `math.ceil()` (arredonda para cima), `math.trunc()` (elimina casas decimais).
  - Conversão de tipos (*Type Casting*): `int()`, `float()`, `str()`.

---

## 🔀 Módulo 3: Lógica e Estruturas Condicionais

- **Operadores de Comparação**: Igualdade (`==`), Diferença (`!=`), Maior que (`>`), Menor que (`<`), Maior ou igual (`>=`), Menor ou igual (`<=`).
- **Operadores Lógicos**:
  - `and`: Exige que todas as condições sejam verdadeiras.
  - `or`: Exige ao menos uma condição verdadeira.
  - `not`: Inverte o valor booleano.
- **Operadores de Pertencimento e Identidade**:
  - `in` / `not in`: Verifica se um valor está presente em uma sequência.
  - `is` / `is not`: Compara se duas variáveis apontam para a mesma posição de memória.
- **Estruturas Condicionais**:
  - Blocos `if`, `elif` e `else` para controle de decisões.
  - Condicional Inline (Operador Ternário): `valor_se_true if condição else valor_se_false`.
  - `match case`: Estrutura para correspondência de padrões e valores exatos.

```python
# Exemplo de fluxo condicional
nota = float(input("Digite a nota: "))

if nota >= 7.0:
    print("Aprovado!")
elif nota >= 5.0:
    print("Recuperação!")
else:
    print("Reprovado!")
```

---

## 🔄 Módulo 4: Estruturas de Repetição (Loops)

- **Loop `while`**: Repete a execução do bloco de código enquanto a condição for verdadeira. O formato `while True` cria um loop contínuo que pode ser interrompido sob uma condição específica.
- **Loop `for`**: Itera sobre sequências ou coleções de dados.
  - Função `range(start, stop, step)`: Gera sequências numéricas iteráveis.
  - Função `enumerate()`: Retorna o índice numérico e o valor correspondente a cada iteração.
- **Comandos de Controle de Fluxo**:
  - `break`: Interrompe e encerra a execução do loop imediatamente.
  - `continue`: Pula o restante do código da iteração atual e passa para a próxima.
  - `pass`: Atua como marcador de posição (*placeholder*) sem alterar o fluxo.
  - Bloco `else` em loops: É executado ao término do loop, desde que não tenha sido interrompido por um `break`.

---

## 📦 Módulo 5: Estruturas de Dados Avançadas (Coleções)

### Tabela Comparativa de Coleções

| Coleção | Sintaxe | Mutável? | Ordenada? | Aceita Duplicatas? | Acesso |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Lista** | `[]` | Sim | Sim | Sim | Índice numérico (``) |
| **Tupla** | `()` | Não | Sim | Sim | Índice numérico (``) |
| **Set (Conjunto)** | `{}` | Sim | Não | Não | Não indexado |
| **Dicionário** | `{chave: valor}` | Sim | Sim | Chaves únicas | Pela Chave (`['chave']`) |

- **Operações com Listas**:
  - Adicionar itens: `append()` (no final), `insert()` (em posição específica).
  - Remover itens: `remove()` (por valor), `pop()` (por índice).
  - Ordenar: `sort()` (modifica a própria lista), `sorted()` (retorna uma nova lista organizada).
- **Desempacotamento de Variáveis (*Unpacking*)**: Atribuição de itens de coleções a variáveis individuais, podendo usar `*` para agrupar múltiplos elementos.
- **Compreensões (*Comprehensions*)**:
  - *List Comprehension*: `[expressão for item in iterável if condição]` para criar e filtrar listas de forma concisa.
  - *Dictionary Comprehension*: `{chave: valor for item in iterável if condição}` para criar dicionários dinâmicos.

---

## ⚙️ Módulo 6: Funções, Boas Práticas e Modularização

- **Criação de Funções (`def`)**: Blocos de código reutilizáveis definidos pela instrução `def`.
  - **Parâmetros e Argumentos**: Parâmetros são declarados na definição; argumentos são os valores informados na chamada.
  - Suporta argumentos posicionais, nomeados (*keyword arguments*) e parâmetros com valores padrão.
  - Parâmetros arbitrários: `*args` (recebe múltiplos argumentos posicionais em uma tupla) e `**kwargs` (recebe múltiplos argumentos nomeados em um dicionário).
  - **Instrução `return`**: Retorna o resultado do processamento da função.
- **Escopo e Expressões Lambda**:
  - Escopo Local (variáveis acessíveis apenas dentro da função) vs Escopo Global (variáveis acessíveis em todo o script).
  - Funções `lambda`: Funções anônimas escritas em uma única linha (`lambda x: expressão`).
- **Padrões de Funções por Propósito**:
  - *Ação*: Executam operações no sistema sem necessariamente retornar valores.
  - *Transformação*: Processam dados de entrada e retornam uma nova estrutura.
  - *Validação*: Checam regras e retornam booleanos (`True`/`False`).
  - *Orquestração*: Coordenam a execução de um fluxo chamando outras funções.
- **Boas Práticas e Legibilidade**:
  - Seguir as recomendações do guia de estilo PEP 8.
  - Documentação com *Docstrings* (`"""docstring"""`) no início de funções.
  - Anotação de tipos (*Type Hints*): `def minha_funcao(parametro: int) -> str:`.
- **Modularização e Módulos Externos**:
  - Divisão de arquivos em módulos e importação via `import` ou `from arquivo import funcao`.
  - Módulos embutidos: `time` (pausas com `time.sleep()`), `random` (geração aleatória com `random.randint()`).
  - Instalação de pacotes de terceiros pelo gerenciador `pip` (ex: `pip install qrcode`, `pip install pillow`).

---

## 🎯 Seção Prática e Próximos Passos

- [ ] **Desafio 1**: Criar um validador completo de e-mail e senha utilizando estruturas condicionais e manipuladores de string.
- [ ] **Desafio 2**: Desenvolver um script para geração automática de QR Codes apontando para links e salvando o arquivo em formato PNG usando a biblioteca `qrcode`.
- [ ] **Desafio 3**: Criar um utilitário de automação para ler, transformar e organizar uma lista de dados.

### 🔗 Referências Oficiais
- [Portal Oficial do Python (python.org)](https://www.python.org/)
- [Documentação Oficial do Python 3](https://docs.python.org/3/)
- [PEP 8 – Guia de Estilo para Código Python](https://peps.python.org/pep-0008/)
- [PyPI – Índice de Pacotes Python](https://pypi.org/)
```

---

💡 Quer testar a execução do script de geração de QR Code ou do validador de e-mails em um arquivo `.py` de exemplo?
