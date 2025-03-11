# ListManipulation
Um repositório dedicado a técnicas para manipulação de listas

## Manipulação de Elementos

### Adicionando um elemento ao final da lista com Append:
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
```
alunos = ["Saldanha", "Borges", "Bayão", "Miguel", "Fonseca", "Ricardo"]
aluno = input("Digite o nome do aluno: ")
alunos.insert(3,aluno)
print(alunos)
```

## Remoção de Elementos

### Removendo elemento na posição especificada (se não for passado um índice, remove o último) com o Pop:
```
alunos = ["Saldanha", "Borges", "Bayão", "Miguel", "Fonseca", "Ricardo"]
aluno = int(input("Digite o índice do aluno a ser excluído: "))
alunos.pop(aluno)
print(alunos)
```
### Removendo a primeira ocorrência do elemento especificado com o Remove:
```
alunos = ["Saldanha", "Borges", "Bayão", "Miguel", "Fonseca", "Ricardo"]
aluno = input("Digite o aluno a ser excluído: ")
alunos.remove(aluno)
print(alunos)
```

## Ordenação

### Ordenando elementos com o Sort:
```
alunos = ["Saldanha", "Borges", "Bayão", "Miguel", "Fonseca", "Ricardo"]
alunos.sort()
print(alunos)
```
### Invertendo a ordem dos elementos com o Reverse:
```
alunos = ["Saldanha", "Borges", "Bayão", "Miguel", "Fonseca", "Ricardo"]
alunos.reverse()
print(alunos)
```

## Contagem

### Retornando o número de vezes que um elemento aparece na lista com o Count:
```
frequencia = []
for i in range(5):
  lancamento = input("O aluno esteve presente? Digite 'P' para presente ou 'F' para falta: ")
  frequencia.append(lancamento.upper())
print(frequencia.count("P"))
```
### Retornando o número de elementos na lista com o Len
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
```
notas = []
for i in range(5):
  nota = float(input("Digite a nota do aluno: "))
  notas.append(nota)
maiorNota = max(notas)
print(maiorNota)
```
### Retornando o menor valor da lista com o Min
```
notas = []
for i in range(5):
  nota = float(input("Digite a nota do aluno: "))
  notas.append(nota)
menorNota = min(notas)
print(menorNota)
```
### Retornando a soma dos elementos da lista com o Sum
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
```
notas = []
for i in range(3):
  nota = float(input("Digite a nota do aluno: "))
  notas.append(nota)
resultado = list(filter(lambda x: x>=7, notas))
print(resultado)
```
### Retornando elementos de uma lista com o Map.
```
notas = []
for i in range(3):
  nota = float(input("Digite a nota do aluno: "))
  notas.append(nota)
resultado = list(map(lambda x: x*2, notas))
print(resultado)
```
Resumo:
filter() pode reduzir o tamanho da lista, pois exclui os elementos que não atendem à condição.
map() sempre mantém o mesmo tamanho da lista, pois aplica uma transformação a todos os elementos sem remover nenhum.

## Consultas avançadas com Filter

### Consultando a partir de um prefixo com o Startswith
```
alunos = ["Saldanha", "Anna Julia Borges", "Bayão", "Julia Ulerich", "Miguel", "Julia Mazala", "Fonseca", "Julia Pinheiro", "Ricardo", "Julia Andrade"]
aluno = input("Digite o nome do aluno que deseja consultar: ")
consulta = list(filter(lambda nome: nome.startswith(aluno), alunos ))
print(consulta)
```

### Consultando a partir de um prefixo com o Endswith
```
alunos = ["Saldanha", "Anna Julia Borges", "Bayão", "Julia Ulerich", "Miguel", "Julia Mazala", "Fonseca", "Julia Pinheiro", "Ricardo", "Julia Andrade"]
aluno = input("Digite o nome do aluno que deseja consultar: ")
consulta = list(filter(lambda nome: nome.endswith(aluno), alunos ))
print(consulta)
```

### Consultando a partir de uma ocorrência com o In
```
alunos = ["Saldanha", "Anna Julia Borges", "Bayão", "Julia Ulerich", "Miguel", "Julia Mazala", "Fonseca", "Julia Pinheiro", "Ricardo", "Julia Andrade"]
aluno = input("Digite o nome do aluno que deseja consultar: ")
consulta = list(filter(lambda nome: aluno in nome, alunos ))
print(consulta)
```

### Consultando a partir de uma ausência com o Not In
```
alunos = ["Saldanha", "Anna Julia Borges", "Bayão", "Julia Ulerich", "Miguel", "Julia Mazala", "Fonseca", "Julia Pinheiro", "Ricardo", "Julia Andrade"]
aluno = input("Digite o nome do aluno que deseja consultar: ")
consulta = list(filter(lambda nome: aluno not in nome, alunos ))
print(consulta)
```
### Consultando a partir de uma lista de dicionários
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





