# SINTAXE BÁSICA KOTLIN

### **MENU DE CONTEÚDOS**
- [**TIPOS DE DADOS**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/Sintaxe-Basica.md#sintaxe-b%C3%A1sica-kotlin)
- [**DECLARAÇÃO DE VARIÁVEL**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/Sintaxe-Basica.md#declara%C3%A7%C3%A3o-de-vari%C3%A1vel)
- [**NULLABILITY**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/Sintaxe-Basica.md#nullability)
- [**OPERADORES ARITMÁTICOS BÁSICOS**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/Sintaxe-Basica.md#operados-aritm%C3%A9ticos-b%C3%A1sicos)
- [**OPERADORES COMPARATIVOS**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/Sintaxe-Basica.md#operados-comparativos)
- [**OPERADORES LÓGICOS**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/Sintaxe-Basica.md#operados-l%C3%B3gicos)
- [**MANIPULAÇÃO DE STRINGS**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/Sintaxe-Basica.md#manipula%C3%A7%C3%A3o-de-strings)
- [**INTRODUÇÃO A FUNÇÕES**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/Sintaxe-Basica.md#introdu%C3%A7%C3%A3o-a-fun%C3%A7%C3%B5es)
- [**ESTRUTURAS DE CONTROLE**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/Sintaxe-Basica.md#estruturas-de-controle)
- [**ESTRUTURAS DE REPETIÇÃO**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/Sintaxe-Basica.md#estruturas-de-repeti%C3%A7%C3%A3o)

---

## - **Tipos de dados**
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

## - **Declaração de Variável**
- **var** -> Variável LOCAL, Valor mutável, CamelCase. Essa variável pode ter o seu valor alterado durante o código.
> Exemplo de declaração: **var currentAge = 22**

- **val** -> Variável LOCAL, Valor imutável, CamelCase. Essa variável terá somente o valor que já foi atribuido, similar ao *final* em Java.
> Exemplo de declaração: **val currentAge = 22**

- **conts val** -> Variável GLOBAL, Valor imutável, SNAKE_CASE. Constante cujo o valor é atribuído durante a compilação.
> Exemplo de declaração: **const val MIN_AGE = 22**

1. Uma variável **não pode** ser declarada **sem tipo ou sem atribuição**;
2. Uma **variável com inferência de tipo** só recerá **valores do mesmo tipo que a sua primeira atribuição**; 
3. Utilizamos o comando **.toString()** para alterar o tipo de dado para uma string, sendo que podemos alterar a palavra String para os outros tipos de que temos e assim fazemos as alterações para esses outros tipos de dados. 

## - **Nullability**

- Qualquer tipo de dado por ser nulo, porém isso deve ser explicitado na declaração de variável através do uso da interrogação (?);
> var month:Int?

- A inferência de tipo não atribui nullability.

## - **Operados Aritméticos Básicos**
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

## - **Operados Comparativos**
- **>** ou **a.compareTo(b)** : maior que

- **<** ou **a.compareTo(b)** : mmenor que

- **>=** ou **a.compareTo(b)** : maior ou igual que

- **<=** ou **a.compareTo(b)** : menor ou igual que

- **==** ou **a.equals(b)** : igual a

- **!=** ou **!(a.equals(b))** : diferente que

1. Os comandos **compareTo** retornam os valores **-1 (menor que), 0 (igual), ou 1 (maior que)**. Já os **operadores** retornam **valores booleanos**;
2. O comando **equals** retorna **valores booleanos**.

## - **Operados Lógicos**
- **(&&)** ou **(expressão1) and (expressão2)** : E

- **(||)** ou **(expressão1) or (expressão2)** : Ou

- **(in)** : contém

- **(!in)** : não contém

- **(Int..Int))** : faixa de valores

1. Quando utiliza-se o **comando**, é recomendado colocar a expressão entre **parenteses**.
2. O retorno é booleano, false ou true.

> Exemplo de código criado por mim usando alguns operadores: [Clique Aqui](https://pl.kotl.in/-OQs26xKk)

## - **Manipulação de Strings**
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

## - **Introdução a Funções**

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

## - **Estruturas de Controle**
1. Temos: if/else, when, elvis operator;
2. Pode ser utilizado tanto para controle quanto para atribuição;
3. Pode ser encadeado com múltiplas estruturas;

> Exemplo **IF/ELSE**:
```
if(expressãoCondicional){
    //bloco de código caso essa condição seja atendida
} else if (outraExpressãoCondicional){
    //bloco de código caso essa condição seja atendida
} else {
    //bloco de código caso nenhuma outra condição seja atendida
}
```

> Exemplo **WHEN**:
```
when {
    expressãoCondicional1 -> {bloco de código caso a condição seja atendida}
    expressãoCondicional2 -> {bloco de código caso a condição seja atendida}
    expressãoCondicional3 -> {bloco de código caso a condição seja atendida}
    expressãoCondicional4 -> {bloco de código caso a condição seja atendida}
    else -> {bloco de código caso nenhuma outra condição seja atendida}
}
```
> Exemplo **ELVIS OPERATOR**:
```
val a:Int? = null
var number = a ?: 0
```

### Atribuição
1. O valor atribuído tem que estar na última linha do bloco;
2. A condicional pode não usar chaves se só fizer a atribuição.

> Exemplo **SEM USAR CHAVES**:
```
val maxValue = if (a > b) a else if (a < b) b else b
```

> Exemplo **USANDO CHAVES**:
```
val minValue = if(a > b){
    println("b($b) é o menor valor")
    b
} else if (a < b){
    println("a($a) é o menor valor")
    a
} else {
    println("os valores são iguais")
    b
}
```

### When
1. Equivalente ao **switch** de outras linguagens;
2. Aceita tanto valores quanto condicionais;
3. Aceita range como case.

> Exemplo 1:
```
when {
    a > b -> {}
    a != b && a > c -> {}
    b == 0 -> {}
    else -> {}
}
```
> Exemplo 2:
```
when(year) {
    -4000..475 -> "Antiguidade"
    476..1452 -> "Medieval"
    1453..1789 -> "Moderna"
    currentYear -> "Tempos atuais"
}
```
### Elvis Operator
1. O mais próximo que a linguagem Kotlin possui de um operador ternário;
2. Verifica se o valor é nulo E apresenta uma opção caso o valor seja nulo;
3. Poder ser encadeado;

> Exemplo:
```
val a:Int? = null
val b:Int? = 9
var number = a?: b?: 0
```
>Nesse caso, se o valor  de **a** não for nulo, o **number** recebe **a**. <br> Se o valor de **a** for nulo e **b** não for nulo, **number** recebe o valor de **b**. <br> Se **a** e **b** forem nulos, **number** recebe o valor 0.

## - **Estruturas de Repetição**
1. Temos as seguintes estruturas: **While, do..while, for e forEach**;
2. Essas estruturas são similares às convencionais em outras linguagens;
3. Aceita os comandos **in, range, until, downTo e step**;

### Como utilizar os comandos
1. **FOR**: `for(variavelIndexadora in/until/downTo faixa de valores/condicional step intervalo)`
2. **IN**: conta do valor inicial até o valor final estabelecido
> Exemplo: `for(i in 0..10)` 
3. **UNTIL**: conta do valor atual até o valor estabelecido -1. Ou seja, se o valor estabelecido for 10, ele contará até 9.
> Exemplo: `for(i in 0 until 10)` 
4. **DOWNTO**: conta de maneira **decrescente**.
> Exemplo: `for(i in 10 downTo 0)` 
5. **STEP**: Determina o intervalo da contagem. Se o step for 2, ele contará de 2 em 2.
> Exemplo: `for(i in 0..10 step 2)`

---
---

**FIM DA ANOTAÇÕES**<br>
Criado por: **Guilherme Speranza**<br>
[LinkedIn - GuiSperanza](https://www.linkedin.com/in/guisperanza/)<br>
[GitHub - GuiSperanza](https://github.com/guisperanza)