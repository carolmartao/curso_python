Python 101

## Introdução

  Python é uma linguagem de programação de propósito geral e se torna um poderoso ambiente para computação científica quando algumas bibliotecas como numpy, matplotlib, scipy e etc auxiliam. No ano de 2020, IEEE Computer Society publicou as linguagens estão emergentes e Python está em primeiro lugar na lista.

  A linguagem Python foi criada em 1991 por um holandês chamado Guido Van Rossumem. Python foi um nome provisório do projeto em que Guido estava envolvido, e este nome vem da série "Monty Python's Flying Circus", da qual Guido era extremamente fã. O intuito do Guido era ter uma linguagem poderosa para desenvolver e administrar sistemas, porém que fosse simples e de fácil entendimento.

  Em outras linguagens, é muito comum o uso intensivo de marcações (;, .), marcadores (chaves, colchetes) e palavras específicas como begin e end. E Python tem legibilidade como uma das principais características, onde o uso destes recursos é reduzido, resultando em uma linguagem limpa e de leitura mais fácil. Python é uma linguagem de alto nível e dinamicamente tipada, é bastante semelhante a um pseudocódigo, onde se pode expressar ideias complexas em poucas linhas de código.

  ### Quem usa Python?
  * Pessoas que já sabem programar
  * Pessoas que querem aprender a programar
  * 80% dos programadores no mundo todo!
  * Python é muito usado em Data Science, AI, Machine Learning, web development e IoT (internet of things).
  * Grandes empresas como Google, NASA, CERN, Facebook, Amazon e Instagram

  ### O que torna Python incrível?
  * Linguágem de propósito genérico
  * Bibliotecas amplamente padronizadas

  ### Quais as Bibliotecas mais interessantes?
  * Pandas, NumPy, SciPy e Matplotlib: computação científica
  * PyTorch, TensorFlow, Keras e Scikit-learn: inteligência artificial
  * Linguagem Natural (NLP) através do Natural Language ToolKit (NLTK)


## Versões de Python

> VERIFICAR AS VERSÕES DISPONÍVEIS

## Tipos de Variáveis

### Numéricos

Semelhante à outras linguagens, Python apresenta tipo inteiro e de ponto flutuante:

```python
x = 8
print (x, type(x))
```

#### Operações 

```python
print (x + 3)   # Adição;
print (x - 3)   # Subtração;
print (x * 3)   # Multiplicação;
print (x ** 3)  # Exponenciação;
```

```python
x += 1
print (x)
x *= 2
print (x)
```

```python
y = x / 2
print (type(y))
print (y, y + 1, y * 2, y ** 2)
```

Veja que Python não tem operadores de incremento e decremento unitário (x++)

> Exercício 1



### Booleanos

### Strings

## Laços

### While

O loop While é uma estrutura de repetição muito simples e funcional, sua vantagem é de suportar varias condições destintas simultaneamente, entretanto este loop precisa de variáveis de controle para que o algoritmo não entre em loop infinito.

```python
y = 3
x = 0

while x < y:
	print(f'X eh menor que Y. {x} < {y}')
	x += 1

```

```flow
st=>start: X = 0
op1=>operation: Print( x = 1 )
X = 1 + 1 = 2
op2=>operation: Print( x = 6 )
X = 2 + 1 = 3
cond=>condition:  Primeira Iteração X < 3 ?
cond1=>condition:  Segunda Iteração X < 3 ?
cond2=>condition: Terceira Iteração X < 3 ?
e=>end

st->cond
cond(true)->op1
op1->cond1
cond1(true)->op2
op2->cond2
cond2(false)->e
```



NOTE QUE: O loop do exemplo acima realiza 2 iterações, ele é um exemplo de um loop **while** com uma condição.

```python	
z = 7
y = 5
x = 0
while x < y and y < z:
	print(f'X eh menor que Y e Y eh menor que Z')
	x += 1
	y += 1

```

NOTE QUE: O loop do exemplo acima realiza 2 iterações, ele é um exemplo de um loop **while** com mais de uma condição.		

### For Loop

O loop For é uma estrutura de repetição bem interessante em Python,  a sua vantagem em relação ao loop **while** é que não precisa da declaração de uma variável de controle e sua sintaxe é bastante simples e versátil.

```python
inicio = 1 
'O inicio é incluido'
final = 10 
'O final não é incluido'
incremento = 5 
'O incremento que vamos fazer para chegar no final'

for x in range(inicio,final,incremento):
	print(f'{x} ')
```

Podemos ver que a estrutura de repetição **for** é bem simples de entender, ela utiliza uma palavra **in** reservada e uma função **range()**, ou seja, semanticamente estamos dizendo **"para  x ** ***no***  **intervalo [ início , final - 1] pulando x de incremento em incremento" ** faça alguma coisa. No caso do exemplo acima o laço vai iterar duas vezes vamos esquematizar:

```flow
st=>start: Inicio X = 1
op1=>operation:  Print( x = 1 )
X = 1 + 5 = 6
op2=>operation: Print( x = 6 )
X = 6 + 5 = 11
cond=>condition: Primeira Iteração X < 10 ?
cond1=>condition: Segunda Iteração X < 10 ?
cond2=>condition: Terceira Iteração X < 10 ?
e=>end

st->cond
cond(true)->op1
op1->cond1
cond1(true)->op2
op2->cond2
cond2(false)->e

```

```python
for x in range(3,20,2):
	print(f'{x} ')
```

Bom o código acima demonstra a definição de um loop for que só escreve no console os números ímpares até 19, a função **range()** pode gerar um tanto intervalo crescente quanto decrescente, vejamos um exemplo a seguir de um **loop** decrescente que imprime no console somente os números pares do intervalo:

```python
for x in range(20,3,-2):
    print(f'{x}')
```

NOTE QUE: Passamos o parâmetro de incremento como negativo, caso contrario o intervalo não será gerado e não vamos iterar no **loop**.

Existe ainda uma ultima maneira de utilizar a função **range()** no loop **for**, passando somente um **int** como parâmetro o intervalo gerado vai de 0 até uma unidade anterior ao parâmetro com incremento unitário:

```python
for x in range(3):
    print(f'{x}')
```

## Containers

## Listas e Vetores
Agora vamos apresentar a estrutura de dados chamada lista, este tipo de estrutura permite armazenar valor de um mesmo tipo de maneira ordenada, no geral coleções de dados são estruturas muito tranquilas de trabalhar em Python, a linguagem  implementa muitas funções nativas e tem uma sintaxe bem versátil para trabalhar com listas. Em linguagens de tipo estático a definição de array é diferente da de lista, um array aloca um espaço de memória contigo e fixo isso significa que uma vez declarado um array nestas linguagens ele vai ocupar aquele espaço na memória até o final da execução do programa ou até um **"coletor de lixo"** ser acionado, enquanto as listas são estruturas dinâmicas no sentido de alocação de memória, podemos adicionar e remover valores dela sem problemas, em Python você não vai ter essa diferenciação, portanto vamos considerar por praticidade que arrays e listas são as mesmas entidades.

NOTA: Python permite que você tenha uma lista com itens de tipo diferentes, mas é importante dizer que você **deve** sempre querer trabalhar com coleções de somente um tipo de dados, isso evita muitos **bugs** no seu código e é uma boa prática em programação, se você esta ciente disso e prefere utilizar essa **"vantagem"** da linguagem use-a com cuidado.

### Declaração de uma Lista:
```python
lista = []
lista = [1,2,3]
lista = ['1', 'a', 'b']
```
NOTE QUE: As declarações feitas acima seguem uma restrição imposta em nossa definição, é uma coleção de elementos ordenados e do mesmo tipo.

Para entendermos melhor as lista é importante saber que elas são estruturas indexadas, ou seja, cada elemento da lista tem uma posição especifica nela que sempre começa no valor 0 e termina no valor n -1 , onde n é o numero de elementos que temos na lista.

### Acesso aos elementos:
```python
lista = [1,2,3,4]
print(lista[0]) 'Escreve no console o valor 1'
print(lista[1]) 'Escreve no console o valor 2'

print(lista[209]) 'Retorna um erro kkkkk'
```

NOTE QUE: O erro ao escrever o item de posição 209 no console já era esperado pois como dito anteriormente só temos acesso ao índice de valor n-1, onde n é o numero de itens da lista.


### Adição Unitária e de Coleções:
```python
lista = []
lista.append(1) 'Adiciona na posição 0 da lista o valor 1'
lista.append(2) 'Adiciona na posição 1 da lista o valor 2'
    
lista.insert(3,2) 'Adiciona na posição 2 da lista o valor 3'

lista[3] = 4 'Adiciona na posição 3 da lista o valor 4'

lista.extend([5,6]) 
'Adiciona na posição 4 e 5 respectivamente os valores 5,6'
    
lista_2 = [7,8,9,10]
    
lista += lista_2
'Concatena a lista com a lista_2, mesmo efeito de extend'

lista_2 *= 2 
'Extende a lista com a própria lista, ou seja, lista_2 = [7,8,9,10,7,8,9,10]''
```
### Remoção Unitária e de Coleções:

```python
lista = [1,2,3,4,5]

ultimo = lista.pop() 'Remove e retorna o ultimo item da lista, ou seja, lista = [1,2,3,4] e ultimo = 5'

lista.remove(2) 'Remove a primeira ocorrencia do valor 2 da lista caso ele exista'
```

### Propriedades e outras funções de Listas:

```python
lista = ["123","456"]
comprimentoDaLista = len(lista)

lista.reverse()
'O ultimos elementos da lista se tornam seus primeiros, ou seja, lista = ["456", "123"]'

lista.sort()
'Ordena os elementos da lista de acordo com o tipo dos elementos, strings alfabeticamente, { int, float } crescente'

lista.sort(reverse=True)
'Ordena os elementos da lista em ordem decrescente de acordo com a implementação do tipo dos elementos'

```

### Percorrendo Listas:

Bom como já passamos pelos Loops vamos ver como utiliza-los para percorrer nossas listas, podemos também realizar operações enquanto percorremos elas, veremos os exemplos abaixo:

```python
lista = [1,2,3,4,5]
for indice in range(len(lista)):
    print(lista[indice])

```

Okay o algoritmo acima é bem simples, ele só escreve no console os elementos da nossa lista, vamos ver exemplos um pouco mais complexos, aplicando filtros, e até mesmo gerando listas de maneira mais simples.

### Geração e Filtragem de Listas:

1-) Gerando uma Lista de 0 até n - 1 sem restrição:

```python
lista = [ x for x in range(0,int(input("Digite o limite da lista: ")))]
```

2-) Gerando uma lista de 0 até n -1 somente com os valores pares:

```python
listaPares = [ x for x in range(0,int(input("Digite o limite da lista: "))) if x % 2 == 0]
```

3-) Gerando uma lista de 0 até n-1 pegando os valores ímpares e elevando-os ao quadrado e os elementos pares multiplicados pelo seu sucessor:

```python
listaMaluca = [x**2 if x % 2 != 0 else x * (x+1) for x in range(0, int(input("Digite o limite da lista: ")))]
```

Os exemplos acima podem sofrer modificações de acordo com suas necessidades, essa sintaxe é muito poderosa e basicamente permite quaisquer operações com os dados durante a geração da lista, aliada com as funções temos uma ferramenta muito poderosa, mas vamos com calma.

Bom vimos nos 3 exemplos acima que gerar listas em Python é super simples, entretanto se já tivermos nossa base de dados armazenada em uma lista em Python como podemos apenas filtra-lá de maneira simples, nos exemplos abaixo vamos simular isso.

1-) Temos uma lista de frutas e queremos filtrar para pegar apenas frutas que o nome comece com uma determinada letra:

```python
frutas = ["maçã","pera","morango","uva","abacate","laranja","mamão"]
letra = input("Digite a letra: ")
'list comprehension'
frutasFiltrada = [fruta for fruta in frutas if fruta[0] == letra]
```

Para resolver o exemplo acima acho interessante apresentar a função **filter()**, ela não é necessária como vimos, entretanto vamos montar um algoritmo com ela para resolver o exemplo 1. Antes de tudo precisamos entender que a função **filter** tem dois parâmetros a função de filtro que retorna um booleano que geralmente é chamada de **predicate** e  a nossa lista que é chamada de **iterable** com esses dois parâmetros a **filter** iterar sobre nossa lista e verificar quais elementos satisfazem nossa condição, ou seja, ela aplica a todos os elementos da lista o nosso **predicate**.

SHOW ME THE CODE KKKK

```python
def Filtro(fruta: str)->bool:
    global letra
    return fruta[0] == letra

lista = ["maçã","pera","morango","uva","abacate","laranja","mamão"]

letra = input("Digite a letra: ")
listaFiltrada = filter(Filtro,lista)
```

Vou apresentar só mais uma versão do código para resolver o exemplo 1, não se preocupe em entender essa ultima abordagem agora, tudo oque você precisa para entender esse exemplo será explicado mais a frente no material, estou apenas mostrando para te motivar a aprender mais sobre Python.

```python
lista = ["maçã","pera","morango","uva","abacate","laranja","mamão"]

letra = input("Digite a letra: ")
listaFiltrada = filter(lambda fruta: True if fruta[0] == letra else False ,lista)
```

Bom como dito anteriormente semanticamente os 3 códigos não tem diferenças, entretanto podemos ver que conseguimos reduzir a quantidade de linhas de nosso programa nos aproveitando da própria sintaxe do Python, leve sempre em consideração reescrever seu código para torna-lo mais legível e simples, algumas dessas ferramentas como o uso do **lambda** e **list comprehension **muitas vezes podem tornar o seu código menos legível, então por mais que eles reduzam as linhas de seu programa se a lógica for muito complexa não são uma boa opção. 

### Map:

### Slicing:

Slicing já é nosso conhecido, realizávamos este tipo de operação com as strings, é mais uma artimanha da sintaxe do Python que nos permite cortar um conjunto de dados, você deve estar pensando qual a semelhança entre **lists** e **arrays** com as **strings** para utilizarmos essa operação de corte, bom vamos te contar um segredo uma **string** nada mais é do que uma lista de **char**, se você não entendeu vamos para os exemplos:

```python
string = "ola"

string_2 = 'o'
string_2 += 'l'
string_2 += 'a'

'string[0] é igual ao char "o" assim como a string_2[0]'

print(string[0:2])
' Escreve no console "ol" , lembrando que [inicio:final], o incio é incluido e o indice final é excluido'

print(string[0:3])
' Escreve no console "ola" '

print(string[::-1])
' Escreve no console "alo" '

'Podemos limitar e fazer o slicing com inversão'
print(string[2:0:-1])
' Escreve no console "al" '
'Lembrando ao utilizar este recurso temos a inversao de "parametros" [final:inicio:-1]'
```

Acima temos uma revisão de ***slicing*** com as strings, vamos ver com os vetores:

```python
vetor = [1,2,3,4]

print(vetor[0:2])
'Escreve no console [1,2]'

print(vetor[::-1])
'Escreve no console [4,3,2,1]'

print(vetor[2:0:-1])
'Escreve no console [4,3]'

```



## Matrizes

## Dicionários

## Sets

## Tuples

## Funções

As funções são como pequenas abstrações mais genéricas no seu código, i.e podemos definir partes menores de nosso algoritmo nomeá-las e parametriza-las, se você já utilizou alguma biblioteca em Python deve ter percebido essa sintaxe **len(array) **, a função **len() ** é nativa da linguagem e retorna o comprimento de uma string,  array etc.

As funções nativas de uma linguagem são funções que não precisam ser definidas pelo programador como a própria função **len()** , entretanto o programador pode definir suas funções, veremos isso nos exemplos a seguir, antes disso é importante entender o porque utilizar funções e como elas podem te ajudar a estruturar melhor seu código e evitar a repetição dele.

1-) Vamos supor que você precisa criar um programa em Python que faça operações básicas com matrizes ambas N x N. Antes de sair escrevendo seu código vamos pensar nas coisas que precisamos fazer para que o algoritmo funcione:
	*Ler Matrizes e armazena-las
	*Escrever o código para as operações (Soma/Subtração)
	*Escrever o código para apresentar o resultado

### Código sem utilizar funções:
```python

numeroDeLinhas = int(input('Insira o numero de Linhas das Matrizes: '))
matriz1 = []
matriz2 = []
resultado = []
aux = 0

'Leitura Da Matriz e Armazenamento'
while aux < 2:
    print(f'\nInsira a Matriz {aux + 1}:')
    for i in range(numeroDeLinhas):
        linha = [int(x) for x in input().strip().split()]
        if aux == 0:
            matriz1.append(linha)
        elif aux == 1:
            matriz2.append(linha)
    aux += 1

'Desvio de Fluxo e Definições de Operações'
operacao = int(input('\n1- Somar || 2-Subtrair: '))

'Definição da Soma'
if operacao == 1:
    resultado = [[matriz1[i][j] + matriz2[i][j]
                 for j in range(len(matriz1[i]))] for i in range(len(matriz1))]

'Definição da Subtração'
elif operacao == 2:
    resultado = [[matriz1[i][j] - matriz2[i][j]
                 for j in range(len(matriz1[i]))] for i in range(len(matriz1))]

'Apresentação do Resultado'
print('\nRESULTADO:')
for linha in resultado:
    print(*linha,sep=' ')

	
```
 O programa acima foi construído sem a utilização das funções, independente se o algoritmo funciona devemos ter cuidado ao programar nossos algoritmos, o exemplo acima não permite o reuso do código, a lógica esta espalhada e não sabemos ao certo oque cada parte do código faz sem que seja realizado um teste de mesa ou a leitura do código.

 DICA: Se você precisa comentar o seu código para entender o seu funcionamento considere reescrever ou revisar o mesmo.

 Algumas mudanças podem deixar o código mais legível, nomes de variáveis e definição de funções são uma delas, vamos escrever o algoritmo utilizando as funções.

Primeiramente devemos entender o uso da palavra reservada **def**, quando utilizamos esta palavra em nosso código estamos dizendo ao interpretador que vamos escrever uma função, logo após a palavra **def**, nomeamos nossa função e parametrizamos ela, portanto **def main()** é a definição de nossa função principal, é importante entender que a função **main** é especial no nosso código, ela que comandara a execução do nosso programa como veremos no exemplo abaixo:

### Sintaxe Das Funções

```python
def main():
	print('Ola mundo')
main()
```

NOTE QUE: O código acima define a função main e chama a mesma para ser executada.

```python
def ParOuImpar(numero: int) -> str:
    if(numero % 2 == 0): return "PAR"
    return "IMPAR"
    
def main():
    numero = int(input("Digite um numero para indentificar sua Paridade: "))
    print(f'{numero} é {ParOuImpar(numero)}')
main()
    
```

NOTE QUE: **ParOuImpar ** é uma função que tem um parâmetro do tipo inteiro e retorna uma string.

```python
def ParOuImpar(numero):
    if(numero % 2 == 0) return "PAR"
	return "IMPAR"

def main():
    numero = int(input("Digite um numero para indentificar sua Paridade: "))
    print(f'{numero} é {ParOuImpar(numero)}')
main()
```

Acima podemos ver que a sintaxe usada na definição de **ParOuImpar** é diferente, entretanto semanticamente não temos diferenças, devemos levar em conta que escrever código é menos trabalhoso que ler, compreender e explicar, logo utilizar a sintaxe mais verbosa dizendo o tipo dos parâmetros e de retorno é interessante pois serve como "documentação" para outros programadores que utilizaram seu código, outras linguagens de programação obrigam a especificação dos tipos então considere utilizar a especificação de tipo se pretende programar em outras linguagens.

 ### Código utilizando funções
 ```python
 
 'Nesta função estamos utilizando a sintaxe mais verbosa onde dizemos qual o tipo de retorno e do parametro'
 
 def LerMatriz(qtdLinhas: int) -> list(list(int)):
    """Le um Matriz de Inteiros"""
    matriz = []
    print("Insira as Linhas da Matriz:")
    for i in range(qtdLinhas):
        linha = [int(x) for x in input().strip().split()]
        matriz.append(linha)
    return matriz

def SomaMatrizes(m1: list(list(int)), m2: list(list(int))) -> list(list(int)):
    """Soma duas Matrizes de Inteiros"""
    return [[m1[i][j] + m2[i][j] for j in range(len(m1[0]))] for i in range(len(m1))]

'Nesta função estamos utilizando a sintaxe menos verbosa onde não especificamos os tipos dos parametros e retorno'

def SubtracaoMatrizes(m1,m2):
    """Subtrai duas Matrizes de Inteiros"""
    return [[m1[i][j] - m2[i][j] for j in range(len(m1[0]))] for i in range(len(m1))]

def ApresentaMatriz(m: list(list(int))) -> None:
    """Apresenta uma Matriz de Inteiros"""
    for linha in m: print(*linha,sep=" ")

'Como dito anteriormente temos a função main que controla a execução do programa'

def main():
    qtdLinhas = int(input("Digite o numero de linhas das Matrizes: "))
    print('\nMATRIZ 1:')
    m1 = LerMatriz(qtdLinhas)
    print('\nMATRIZ 2:')
    m2 = LerMatriz(qtdLinhas)
    
    print('\nSOMA DE MATRIZES:')
    ApresentaMatriz(SomaMatrizes(m1,m2))
    
'Assim chamamos uma função main'
main()
 	
 ```

NOTE QUE: Escrevemos comentários com 3 aspas duplas abaixo das definições, isso permite que programadores que vão utilizar nosso métodos leiam e compreendam seu funcionamento, além disso se você for um programador legal e explicitar os tipos de parâmetros e retorno essas informações também aparecem nessa pequena documentação, mas atenção essa documentação deve ser sempre sucinta e objetiva.

Podemos perceber que o nível de organização do código acima é melhor quando comparado ao anterior, existem algumas variações na sintaxe da definição das funções em Python, anteriormente foi apresentado no item de **Listas e Vetores** a sintaxe e uso de funções lambda, vamos reescrever o algoritmo do exercício das matrizes com esse recurso, levantar alguns questionamentos e concluir este tópico.

Antes de qualquer coisa vamos apresentar a sintaxe das funções lambda:

1-) Criar uma expressão lambda para verificar paridade de um numero:

```python
fParidade = lambda numero: "PAR" if numero % 2 == 0 else "IMPAR"
```

NOTE QUE: Ao utilizarmos a palavra reservada **lambda** devemos nomea-la atribuindo-a para uma variável no exemplo acima nomeamos-a **fParidade**, logo após a palavra reservada devemos escrever os parâmetros da função, ou seja, nossa função lambda acima é uma função que tem somente um parâmetro chamado **numero**, após dizermos os parâmetros definimos a função depois do caractere **'' : ''** , no exemplo acima utilizamos uma estrutura condicional para definir o retorno, quando utilizamos um condicional em uma expressão **lambda** devemos primeiro escrever o retorno para a condição verdadeira, em seguida a condição com **if** e por fim a palavra reservada **else** e o retorno se falsa.

2-) Criar uma expressão lambda que tenha dois parâmetros **x** e **y** e retorne **x**^**y** :

```python
fPotencia = lambda x,y : x ** y
```

Acima temos uma expressão **lambda** com mais de um parâmetro, teoricamente podemos definir quantos parâmetros quisermos, mas perceba que o intuito desta sintaxe é definir funções simples sem precisar usar uma definição mais verbosa como **def**. 

### Código utilizando Funções / Expressões Lambda 

Bom com essa pequena introdução acima vamos reescrever o exercício das matrizes somente com expressões lambda, vamos ver na pratica quando utiliza-las  e quando não.

SHOW ME THE CODE KKK:

```python

LerLinha = lambda : list(map(lambda elemento: int(elemento) ,input().strip().split()))

LerMatriz = lambda qtdLinhas: list(map(lambda matriz: list(map(lambda linha: linha,LerLinha())),range(qtdLinhas)))

SomaMatrizes = lambda m1,m2: list(map(lambda x: list(map(lambda y: m1[x][y] + m2[x][y], range(len(m1[0])))),range(len(m1))))

SubtraiMatrizes = lambda m1,m2: list(map(lambda x: list(map(lambda y: m1[x][y] - m2[x][y], range(len(m1[0])))),range(len(m1))))

ApresentaMatriz = lambda matriz: [print(*linha,sep=" ") for linha in matriz]

def main():
    qtdLinhas = int(input("Digite o numero de Linhas da Matriz: "))
    print('\nMATRIZ 1:')
    m1 = LerMatriz(qtdLinhas)
    print('\nMATRIZ 2:')
    m2 = LerMatriz(qtdLinhas)

    print('\nSOMA DE MATRIZES:')
    ApresentaMatriz(SomaMatrizes(m1,m2))  

    print('\nSUBTRAÇÃO DE MATRIZES:')
    ApresentaMatriz(SubtraiMatrizes(m1,m2))

main()
```

Não se assunte se você não entendeu o código acima, ele é um exemplo de abuso do uso de expressões **lambda**, o primeiro questionamento que você deve fazer ao escrever um código é se ele é legível, olhando para o código acima é muito difícil entender oque cada função faz sem realizar a leitura de seus nomes, outro problema é a composição de expressões **lambda**, assim como a definição de funções dentro de funções é uma pratica ruim a composição de **lambdas** também é, a conclusão é que devemos ter bom senso ao tentar reduzir as linhas de nosso programa, devemos sempre nos preocupar com a **legibilidade** e **simplicidade** da nossa solução, e por fim a documentação vimos que quando utilizamos a palavra reservada **def** podemos usar um comentário com 3 aspas duplas para dar uma noção aos outros programadores sobre o funcionamento do nosso método além disso vimos que podemos explicitar os tipos dos parâmetros e retorno de nossas funções, ambas as operações não são possíveis com a a sintaxe **lambda**.

#### *“Qualquer tolo consegue escrever código que um computador entenda. Bons programadores escrevem código que humanos possam entender.”*

#### Martin Fowler




## Classes

> Teste
