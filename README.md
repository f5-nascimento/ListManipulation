# ListManipulation
Um repositório dedicado a técnicas para manipulação de listas

## Manipulação de Elementos

### Adicionando um elemento ao final da lista com Append:
Este método adiciona um novo item ao final de uma lista. É útil para acumular elementos em uma lista durante a execução do código.
```
alunos = []
while True:
  aluno = input("Digite o nome do aluno (ou 'sair' para encerrar): ")
  if aluno.lower() == 'sair':
    break
  alunos.append(aluno)
print(alunos)
```
### Inserindo um elemento em uma posição específica com o Insert:
O insert() permite adicionar um elemento em uma posição específica da lista, deslocando os outros elementos para a direita.
```
alunos = ["Saldanha", "Borges", "Bayão", "Miguel", "Fonseca", "Ricardo"]
aluno = input("Digite o nome do aluno: ")
alunos.insert(3,aluno)
print(alunos)
```

## Remoção de Elementos

### Removendo elemento na posição especificada (se não for passado um índice, remove o último) com o Pop:
Com o pop(), podemos remover um item da lista pela sua posição, e ele também retorna o valor removido.
```
alunos = ["Saldanha", "Borges", "Bayão", "Miguel", "Fonseca", "Ricardo"]
aluno = int(input("Digite o índice do aluno a ser excluído: "))
alunos.pop(aluno)
print(alunos)
```
### Removendo a primeira ocorrência do elemento especificado com o Remove:
O remove() elimina a primeira ocorrência do elemento fornecido, sem precisar especificar a posição.
```
alunos = ["Saldanha", "Borges", "Bayão", "Miguel", "Fonseca", "Ricardo"]
aluno = input("Digite o aluno a ser excluído: ")
alunos.remove(aluno)
print(alunos)
```

## Ordenação

### Ordenando elementos com o Sort:
A função sort() organiza os elementos da lista em ordem crescente, alterando a própria lista.
```
alunos = ["Saldanha", "Borges", "Bayão", "Miguel", "Fonseca", "Ricardo"]
alunos.sort()
print(alunos)
```
### Invertendo a ordem dos elementos com o Reverse:
O reverse() inverte os elementos de uma lista, mudando a ordem dos itens para o contrário.
```
alunos = ["Saldanha", "Borges", "Bayão", "Miguel", "Fonseca", "Ricardo"]
alunos.reverse()
print(alunos)
```

## Contagem

### Retornando o número de vezes que um elemento aparece na lista com o Count:
Com o count(), podemos verificar quantas vezes um elemento específico ocorre dentro de uma lista.
```
frequencia = []
for i in range(5):
  lancamento = input("O aluno esteve presente? Digite 'P' para presente ou 'F' para falta: ")
  frequencia.append(lancamento.upper())
print(frequencia.count("P"))
```
### Retornando o número de elementos na lista com o Len
O len() retorna a quantidade total de elementos dentro de uma lista.
```
alunos = ["Saldanha", "Borges", "Bayão", "Miguel", "Fonseca", "Ricardo"]
while True:
  aluno = input("Digite o nome do aluno (ou 'sair' para encerrar): ")
  if aluno.lower() == 'sair':
    break
  alunos.append(aluno)
qtdAlunos = len(alunos)
print(qtdAlunos)
```
### Retornando o maior valor da lista com o Max
O max() encontra e retorna o maior valor presente em uma lista de números.
```
notas = []
for i in range(5):
  nota = float(input("Digite a nota do aluno: "))
  notas.append(nota)
maiorNota = max(notas)
print(maiorNota)
```
### Retornando o menor valor da lista com o Min
Similar ao max(), o min() retorna o menor valor presente na lista.
```
notas = []
for i in range(5):
  nota = float(input("Digite a nota do aluno: "))
  notas.append(nota)
menorNota = min(notas)
print(menorNota)
```
### Retornando a soma dos elementos da lista com o Sum
Com o sum(), podemos somar todos os valores numéricos em uma lista.
```
notas = []
for i in range(5):
  nota = float(input("Digite a nota do aluno: "))
  notas.append(nota)
somarNotas = sum(notas)
print(somarNotas)
```
## Consultas

### Retornando o índice da primeira ocorrência do elemento especificado com o Index.
O index() retorna a posição do primeiro elemento encontrado na lista que corresponde ao valor fornecido.
```
alunos = ["Saldanha", "Borges", "Bayão", "Miguel", "Fonseca", "Ricardo"]
while True:
  aluno = input("Digite o nome do aluno (ou 'sair' para encerrar): ")
  if aluno.lower() == 'sair':
    break
  indice = alunos.index(aluno)
  print(indice)
```
### Retornando elementos de uma lista com o Filter.
O filter() permite criar uma nova lista contendo somente os elementos que atendem a uma condição específica.
```
notas = []
for i in range(3):
  nota = float(input("Digite a nota do aluno: "))
  notas.append(nota)
resultado = list(filter(lambda x: x>=7, notas))
print(resultado)
```
### Retornando elementos de uma lista com o Map.
O map() aplica uma função a cada elemento de uma lista, transformando os valores sem remover itens.
```
notas = []
for i in range(3):
  nota = float(input("Digite a nota do aluno: "))
  notas.append(nota)
resultado = list(map(lambda x: x*2, notas))
print(resultado)
```

### Resumo:
- filter() pode reduzir o tamanho da lista, pois exclui os elementos que não atendem à condição.
- map() sempre mantém o mesmo tamanho da lista, pois aplica uma transformação a todos os elementos sem remover nenhum.

## Consultas avançadas com Filter

### Consultando a partir de um prefixo com o Startswith
O startswith() filtra elementos que começam com o prefixo especificado.
```
alunos = ["Saldanha", "Anna Julia Borges", "Bayão", "Julia Ulerich", "Miguel", "Julia Mazala", "Fonseca", "Julia Pinheiro", "Ricardo", "Julia Andrade"]
aluno = input("Digite o nome do aluno que deseja consultar: ")
consulta = list(filter(lambda nome: nome.startswith(aluno), alunos ))
print(consulta)
```

### Consultando a partir de um prefixo com o Endswith
O endswith() filtra elementos que terminam com o sufixo especificado.
```
alunos = ["Saldanha", "Anna Julia Borges", "Bayão", "Julia Ulerich", "Miguel", "Julia Mazala", "Fonseca", "Julia Pinheiro", "Ricardo", "Julia Andrade"]
aluno = input("Digite o nome do aluno que deseja consultar: ")
consulta = list(filter(lambda nome: nome.endswith(aluno), alunos ))
print(consulta)
```

### Consultando a partir de uma ocorrência com o In
O operador in permite filtrar elementos que contêm uma certa substring.
```
alunos = ["Saldanha", "Anna Julia Borges", "Bayão", "Julia Ulerich", "Miguel", "Julia Mazala", "Fonseca", "Julia Pinheiro", "Ricardo", "Julia Andrade"]
aluno = input("Digite o nome do aluno que deseja consultar: ")
consulta = list(filter(lambda nome: aluno in nome, alunos ))
print(consulta)
```

### Consultando a partir de uma ausência com o Not In
O operador not in filtra os elementos que não contêm a substring especificada.
```
alunos = ["Saldanha", "Anna Julia Borges", "Bayão", "Julia Ulerich", "Miguel", "Julia Mazala", "Fonseca", "Julia Pinheiro", "Ricardo", "Julia Andrade"]
aluno = input("Digite o nome do aluno que deseja consultar: ")
consulta = list(filter(lambda nome: aluno not in nome, alunos ))
print(consulta)
```
### Consultando a partir de uma lista de dicionários
Aqui, map() e filter() são usados em conjunto para filtrar elementos de uma lista de dicionários com base em uma condição e extrair um valor específico (neste caso, o nome do aluno).
```
alunos = [
    {
        "nome": "Rafael",
        "nota": 10
    },
    {
        "nome": "Baltar",
        "nota": 7
    },
    {
        "nome": "Vieira",
        "nota": 5
    }
]

aprovados = list(map(lambda aluno: aluno["nome"], filter(lambda x: x["nota"]>=7, alunos )))
print(aprovados)
```





