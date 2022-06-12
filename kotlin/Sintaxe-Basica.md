# SINTAXE BÁSICA KOTLIN

## Tipos de dados
- **long** : Números Inteiros (64 bits)
- **int** : Números Inteiros (32 bits)
- **short** : Números Inteiros (16 bits)
- **byte** : Números Inteiros (8 bits)
- **double** : Números Reais/Decimais (64 bits)
- **float** : Números Reais/Decimais (32 bits)
- **boolean** : Verdadeiro ou Falso
- **char** : Caracteres
- **array** : Matrizes
- **null!** ->

## Declaração de Variável
- **var** -> Variável LOCAL, Valor mutável, CamelCase. Essa variável pode ter o seu valor alterado durante o código.
> Exemplo de declaração: **var currentAge = 22**

- **val** -> Variável LOCAL, Valor imutável, CamelCase. Essa variável terá somente o valor que já foi atribuido, similar ao *final* em Java.
> Exemplo de declaração: **val currentAge = 22**

- **conts val** -> Variável GLOBAL, Valor imutável, SNAKE_CASE. Constante cujo o valor é atribuído durante a compilação.
> Exemplo de declaração: **const val MIN_AGE = 22**

1. Uma variável **não pode** ser declarada **sem tipo ou sem atribuição**;
2. Uma **variável com inferência de tipo** só recerá **valores do mesmo tipo que a sua primeira atribuição**; 
3. Utilizamos o comando **.toString()** para alterar o tipo de dado para uma string, sendo que podemos alterar a palavra String para os outros tipos de que temos e assim fazemos as alterações para esses outros tipos de dados. 

## Nullability

- Qualquer tipo de dado por ser nulo, porém isso deve ser explicitado na declaração de variável através do uso da interrogação (?);
> var month:Int?

- A inferência de tipo não atribui nullability.

## Operados Aritméticos Básicos
- **+** ou **a.plus(b)** : soma
> Para atribuição, usamos: a +=b

- **-** ou **a.minus(b)** : subtração
> Para atribuição, usamos: a -=b

- **'*'** ou **a.times(b)** : multiplicação
> Para atribuição, usamos: a *=b

- **/** ou **a.div(b)** : divisão
> Para atribuição, usamos: a /=b

- **%** ou **a.mod(b)** : resto
> Para atribuição, usamos: a %=b

1. Os operadores podem ser chamados tanto como expressão quanto como comando.;
2. O operador **+** também serve para concatenar String;
3. Na **Atribuição**, o valor de A passa a receber o resultado da operação.

## Operados Comparativos
- **>** ou **a.compareTo(b)** : maior que

- **<** ou **a.compareTo(b)** : mmenor que

- **>=** ou **a.compareTo(b)** : maior ou igual que

- **<=** ou **a.compareTo(b)** : menor ou igual que

- **==** ou **a.equals(b)** : igual a

- **!=** ou **!(a.equals(b))** : diferente que

1. Os comandos **compareTo** retornam os valores **-1 (menor que), 0 (igual), ou 1 (maior que)**. Já os **operadores** retornam **valores booleanos**;
2. O comando **equals** retorna **valores booleanos**.

## Operados Lógicos
- **E** ou **(&&)** ou **(expressão1) and (expressão2)** : E

- **Ou** ou **(||)** ou **(expressão1) or (expressão2)** : Ou

- **contém** ou **(in)** : contém

- **não contém** ou **(!in)** : não contém

- **range** ou **(Int..Int))** : faixa de valores

1. Quando utiliza-se o **comando**, é recomendado colocar a expressão entre **parenteses**.
2. O retorno é booleano, false ou true.

> Exemplo de código criado por mim usando alguns operadores: [Clique Aqui](https://pl.kotl.in/OIdNID82A)