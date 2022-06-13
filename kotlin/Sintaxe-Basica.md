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

> Exemplo de código criado por mim usando alguns operadores: [Clique Aqui](https://pl.kotl.in/-OQs26xKk)

## Manipulação de Strings
1. Strings possuem diversos métodos associados:
> Indexação, concatenação, comparação e formatação;
2. Strings podem ser concatenadas com plus/+;
3. String e Variáveis podem ser concatenadas com `${}` (quando adicionados um método) ou apenas `$` antes das variáveis;
4. Também é tratada como um array de Char;


### Alguns Métodos de Associação/Indexação
- **First()** : Acessa a primeira posição do array
- **last()** : Acessa a última posição do array
- **String.lenght** : Informa o número de posições da array
- **String[index]** : Acessa a posição solicitada

### Alguns Métodos de Formatação
- **capitalize(), toUpperCase(), toLowerCase(), decapitalize()** : Capitalização de Strings
> capitalize() muda a primeira letra para maiúscula. toUpperCase faz com que todas as letras fiquem maiúsculas. toLowerCase faz com que todas as letras fiquem minúsculas. decapitalize faz com que a primeira letra fique minúscula.

- **trimEnd(), trimStart(), trim()** : Remoação de Espaços vazios e caracteres inadequados para impressão
> trimEnd retira o espaço final. trimStart retira o espaço inicial.

- **replace(x,y)** : Substituição de caracteres

- **"padrão ${x}".format(x)** : Utilizado para criar uma formatação padrão

## Introdução a Funções

1. Começamos as funções da seguinte maneira : `fun nomeDaFunção(nome:tipoDeDado):tipoDoRetorno{}`
> Exemplo in-line: `fun getFullName(name:String, lastName:String) = "$name $lastName" ` <br>
> Exemplo 2: `private fun getFullName(name:String, lastName:String):String {return "$name $lastName"} `

### Funções ordem superior
1. Recebem outra função ou lambada por parâmetro;
2. Bastante úteis para a generalização de funções e tratamento de erros;
> Exemplo 1: `val x = calculate{12,34,::sum} ` : a função irá somar 12 e 34. <br>
> Exemplo 2: `val x = calculate{12,34}{a, b -> a+b} ` : a função irá somar 12 e 34.

### Funções single-line
1. Prefixo **Fun nomeDaFunção(nome:tipoDeDado) = retorno**;
2. São funções de uma única linha;
3. Infere o tipo de retorno.
> Exemplo: `private fun getFullName(name:String, lastName:String) = "$name $lastName"`

### Funções/Extensões
1. Prefixo **Fun tipoDeDado.nomeDaFunção()**
2. Cria uuma função que só pode ser chamada por um tipo específico de dado, cujo valor pode ser referenciado dentro da função através da palavra **this**.
> Exemplo: `fun String.randomLetter() = this [(0..this.length-1).random()].toUpperCase()`

## Estruturas de Controle

