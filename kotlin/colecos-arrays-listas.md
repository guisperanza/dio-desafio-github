# COLEÇÕES, ARRAYS, LIST, SET and MAP

### **MENU DE CONTEÚDOS**
- [**CONCEITOS SOBRE COLEÇÕES**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--conceitos-sobre-cole%C3%A7%C3%B5es)<br> 
    -> [**Como Criar uma Coleção**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--como-criar-cole%C3%A7%C3%B5es)

<br>

- [**ARRAY**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--array)<br> 
    -> [**IntArray/intArrayOf**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--intarrayof)<br>
    -> [**Array/arrayOf**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--array-de-string)<br>
    -> [**DoubleArray/doubleArrayOf**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--double-array)<br>

<br>

- [**OPERAÇÕES COM ARRAY**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--opera%C3%A7%C3%B5es-com-array)<br>
    -> [**sort()**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--sort)<br>
    -> [**max, min e average**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--max-min-e-average)<br>
    -> [**filter**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--filter)<br>
    -> [**count, find e any**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--array-count-find-e-any)<br>
    -> [**listOf**]()<br>
    -> [**sortedBy**]()<br>
    -> [**groupBy**]()<br>
    -> [**setOf**]()<br>
    -> [**mapOf**]()

<br>

- [**OPERAÇÃO ou MÉTODO COLETOR**]()

---
## - **CONCEITOS SOBRE COLEÇÕES**

1. O Kotlin **não possui** o seu próprio conjuntos de coleções (List, Map, Set, etc);
2. Kotlin **usa as classes de coleção Java Padrão**;
3. É muito simples criar uma coleção com Kotlin
> Exemplo usando ArrayList: `val frutas = arrayListOf("Maçã", "Banana","Morango")` 
4. Apesar do Kotlin não ter o seu próprio conjunto de coleções, é possível fazer muito mais com as coleções em Kotlin.

### - **COMO CRIAR COLEÇÕES**

- Exemplo Java:
```
fun main() {
    val frutas1 = ArrayList<String>()
    frutas1.add("Maçã")
    frutas1.add("Banana")
    frutas1.add("Morango")
    
 	println(frutas1)
        
}
```
- Exemplo Kotlin:
```
fun main() {
    val frutas = arrayListOf("Maçã", "Banana", "Morango")
    
 	println(frutas)
        
}
```

- Usar Kotlin para criar coleções, como já dito antes, é **mais simples**.





Fonte: Canal Douglas Motta - [Link Clicando Aqui](https://youtu.be/IVFZhFdC0KI)


## - **ARRAY**
1. Array é uma forma de gravar um registro de mesmo tipo que pode ser acessado por índice;
2. O indice sempre começa pelo índice O;
3. O índice máximo de uma array é sempre "o tamanho escolhido" -1. Exemplo: Se você declarar o valor 5 como tamanho da array, o indice final será o 4.

- Exemplo de Array: 
```
fun main() {
    val values = IntArray(5)
    values[0] = 1
    values[1] = 7
    values[2] = 6
    values[3] = 3
    values[4] = 2
    
    for (valor in values) { //Primeira opção para iterar a array
        println(valor)
    }
    
       println("-------")
     
    values.forEach { //Segunda opção para iterar a array
        println(it)
    }
       println("-------")
       
    for (index in values.indices) { //Terceira opção para iterar a array
        println(values[index])
    }

}
```
> Link para o code no Kotlin Playground: [Clique Aqui](https://pl.kotl.in/BOiCFB11o)

### - **intArrayOf**
1. Podemos utilizar o `intArrayOf()` para criar uma array sem a necessidade de declarar o seu "tamanho".
   
   - Exemplo:
```
fun main() {
    val values = intArrayOf(5, 2, 10, 14, 23)
    
    for (valor in values) {
        println(valor)
    }
}
```
### - **Array de String**

> Exeplo com **MAIS** linhas de código
```
fun main() {
    val nomes = Array(3){""}
       nomes[0] = "Maria"
       nomes[1] = "Felipe"
       nomes[2] = "José" 
    
    nomes.sort()
    nomes.forEach {println(it)}
}
```

> Exeplo com **MENOS** linhas de código
```
fun main() {
    val nomes = arrayOf("Gui", "Weverton", "Maria")
   
    nomes.forEach{println(it)}
    }
```
1. Usamos o `arrayOf` e o `intArrayOf` com o objetivo de economizar linhas de código. 

### - **Double Array e doubleArrayOf**
```
fun main() {
    val salarios = DoubleArray(3)
    salarios[0] = 1000.0
    salarios[1] = 5000.0
    salarios[2] = 500.0  
   
    salarios.sort()
    salarios.forEach{ println(it) }
    }
```

> Usando o `doubleArrayOf`

```
fun main() {
    val salarios = doubleArrayOf(1000.0, 3000.0, 500.0)
  
    salarios.sort()
    salarios.forEach{ println(it) }
}
```


<BR> 

## - **OPERAÇÕES COM ARRAY**

### - **.SORT()**
Podemos utilizar o comando `.sort()` para colocar a array com os seus valores em forma crescente

- Exemplo:

```
fun main() {
    val values = IntArray(5)
    values[0] = 1
    values[1] = 7
    values[2] = 6
    values[3] = 3
    values[4] = 2
    
    values.sort()
    for (valor in values) {
        println(valor)
    }
    
}
```

### - **MAXORNULL, MINORNULL e AVERAGE**
``` 
fun main() {
    val barra:String = "------------------"
    val salarios = doubleArrayOf(1000.0, 3000.0, 500.0)
  
    for (salario in salarios){
        println(salario)
    }
    
    println(barra)
    
    println("O maior salário é: R$ ${salarios.maxOrNull()}") //Retorna o maior valor da array
    println("O menor salário é: R$ ${salarios.minOrNull()}") //Retorna o menor valor da array
    println("A média salarial é: R$ ${salarios.average()}") //Retorna a média dos valores da array    
  
}
```
### - **FILTER**
```
fun main() {
    val barra:String = "------------------"
    val salarios = doubleArrayOf(1000.0, 3000.0, 500.0)
  
    for (salario in salarios){
        println("Salário: R$ $salario")
    }
     
    val salariosMaiorQue2500 =  salarios.filter { it > 2500 } //Usamos IT e não SALARIOS nesse caso porque estamos utilizando a iteração por meio do FOR/FOREACH
    println(barra)
    salariosMaiorQue2500.forEach { println("Os salários maiores que R$ 2.500 são: R$ $it")}
  
}
```
### - **ARRAY COUNT, FIND e ANY**
```
fun main() {
    val barra:String = "-------------"
    val salarios = doubleArrayOf(1000.0, 3000.0, 500.0)
  
    for (salario in salarios){
        println("Salário: R$ $salario")
    }
    println(barra)
    println(salarios.count { it in 2000.0..5000.0}) //Retorna a quantidade de valores entre 2.000 e 5.0000
        println(barra)

    println(salarios.find { it == 3000.0}) //Busca e Retorna o valor 3000.0 caso ele seja um valor na array
        println(barra)

    println(salarios.any { it >= 3000.0}) //Retorna um valor booleano para a expressão

}
```
### - **ListOF**
- Usado para criar uma lista na collection
```
fun main() {
    val joao = Funcionarios(nome = "João", salario = 1500)
    val pedro = Funcionarios(nome = "Pedro", salario = 5000)
    val maria = Funcionarios(nome = "Maria", salario = 3500)

    val barra: String = "------------------"
    
    val funcionarios = listOf(joao, pedro, maria)
  
    funcionarios.forEach{ println(it)}
    
    println(barra)
    
    println(funcionarios.find { it.nome == "Maria"}) //Busca na lista e retorna apenas a condição verdadeira
  
}

data class Funcionarios (
	val nome: String,
	val salario: Int
) {
    override fun toString():String = """
    Nome: $nome
    Salário: R$ $salario
    
    """.trimIndent()
}
```
### - **SortedBy**
- Usado para colocar os valores das collections em ordem crescente seguindo uma condição

```
fun main() {
    val joao = Funcionarios(nome = "João", salario = 1500, tipoDeContratacao = "PF")
    val pedro = Funcionarios(nome = "Pedro", salario = 5000, tipoDeContratacao = "PF")
    val maria = Funcionarios(nome = "Maria", salario = 3500, tipoDeContratacao = "PJ")

    val barra: String = "------------------"
    
    val funcionarios = listOf(joao, pedro, maria)
  
    funcionarios
        .forEach { println(it) }
       
    println(barra)
    
    funcionarios
        .sortedBy { it.salario }
        .forEach { println(it) }
  
}

data class Funcionarios (
	val nome: String,
	val salario: Int,
    val tipoDeContratacao: String
) {
    override fun toString():String = """
    Nome: $nome
    Salário: R$ $salario
    Tipo de Contratação: $tipoDeContratacao
    
    """.trimIndent()
}
```
### - **GroupBy**
1. Usado para agrupos collections sob uma mesma condição;
2. Podemos ou não declarar uma condição de agrupamento;
   > Exemplo: `.groupBy { it.tipoDeContratacao == "CLT" }` ou `.groupBy { it.tipoDeContratacao }` 
3. Quando agrupamos, um **MAPA É CRIADO**.
```
fun main() {
    val joao = Funcionarios(nome = "João", salario = 1500, tipoDeContratacao = "CLT")
    val pedro = Funcionarios(nome = "Pedro", salario = 5000, tipoDeContratacao = "CLT")
    val maria = Funcionarios(nome = "Maria", salario = 3500, tipoDeContratacao = "PJ")

    val barra: String = "------------------"
    
    val funcionarios = listOf(joao, pedro, maria)
  
    funcionarios.forEach{ println(it)}
    
   	println(barra)
        
    funcionarios
        .groupBy { it.tipoDeContratacao == "CLT" }  // Agrupar sob a condição de Contratação "CLT"
        .forEach { println(it) } 

}

data class Funcionarios (
	val nome: String,
	val salario: Int,
    val tipoDeContratacao: String
) {
    override fun toString():String = """
    Nome: $nome
    Salário: R$ $salario
    Tipo de Contratação: $tipoDeContratacao
    
    """.trimIndent()
}
```
### - **setOf**
1. Usado para criar conjuntos diferentes para objetos com características específicas;
2. É diferente do `listOf()` onde colocamos todos os objetos juntos;

>Exemplo básico com o uso do comando `x.union(y)`: usado para unir dois conjuntos diferentes

```
fun main() {
    val joao = Funcionarios(nome = "João", salario = 1500, tipoDeContratacao = "CLT")
    val pedro = Funcionarios(nome = "Pedro", salario = 5000, tipoDeContratacao = "CLT")
    val maria = Funcionarios(nome = "Maria", salario = 3500, tipoDeContratacao = "PJ")

    val barra: String = "------------------"
    
    val funcionariosCLT = setOf(joao, pedro)
    val funcionariosPJ = setOf(maria)
  
    val resultUnion = funcionariosCLT.union(funcionariosPJ)
    
    resultUnion.forEach{ println(it) }    
          
}

data class Funcionarios (
	val nome: String,
	val salario: Int,
    val tipoDeContratacao: String
) {
    override fun toString():String = """
    Nome: $nome
    Salário: R$ $salario
    Tipo de Contratação: $tipoDeContratacao
    
    """.trimIndent()
}
```
>Exeplo usando a operação `x.minus(y)`: usado para subtrair um conjunto X de outro Y

```
fun main() {
    val joao = Funcionarios(nome = "João", salario = 1500, tipoDeContratacao = "CLT")
    val pedro = Funcionarios(nome = "Pedro", salario = 5000, tipoDeContratacao = "CLT")
    val maria = Funcionarios(nome = "Maria", salario = 3500, tipoDeContratacao = "PJ")

    val barra: String = "------------------"
    
    val funcionariosCLT = setOf(joao, pedro)
    val funcionariosPJ = setOf(maria)
  
    val resultUnion = funcionariosCLT.union(funcionariosPJ) //.Union é usado para unir dois conjuntos diferentes
    
    resultUnion.forEach{ println(it) }  
    
    println(barra)
    val funcionariosTodos = setOf(joao, pedro, maria)
    val resultSubtract = funcionariosTodos.minus(funcionariosPJ)
    
    resultSubtract.forEach{ println(it) } 
    
          
}

data class Funcionarios (
	val nome: String,
	val salario: Int,
    val tipoDeContratacao: String
) {
    override fun toString():String = """
    Nome: $nome
    Salário: R$ $salario
    Tipo de Contratação: $tipoDeContratacao
    
    """.trimIndent()
}
```
>Exemplo usando o comando `x.intersect(y)` : usado para encontrar valores em comum nos conjuntos X e Y

```
fun main() {
    val joao = Funcionarios(nome = "João", salario = 1500, tipoDeContratacao = "CLT")
    val pedro = Funcionarios(nome = "Pedro", salario = 5000, tipoDeContratacao = "CLT")
    val maria = Funcionarios(nome = "Maria", salario = 3500, tipoDeContratacao = "PJ")

    val barra: String = "------------------"
    
    val funcionariosCLT = setOf(joao, pedro)
    val funcionariosPJ = setOf(maria)
  
    val resultUnion = funcionariosCLT.union(funcionariosPJ) //.Union é usado para unir dois conjuntos diferentes
    
    resultUnion.forEach{ println(it) }  
    
    println(barra)
    val funcionariosTodos = setOf(joao, pedro, maria)
    val resultIntersect = funcionariosTodos.intersect(funcionariosPJ)
    
    resultIntersect.forEach{ println(it) } 
    
          
}

data class Funcionarios (
	val nome: String,
	val salario: Int,
    val tipoDeContratacao: String
) {
    override fun toString():String = """
    Nome: $nome
    Salário: R$ $salario
    Tipo de Contratação: $tipoDeContratacao
    
    """.trimIndent()
}
```
### - **mapOf**
1. Um mapa é uma coleção de **chaves** e **valores**;

```
fun main() {
    //Primeira maneira de criar um mapa
    val pair: Pair<String, Double> = Pair("João", 1000.0)
    val map1= mapOf(pair)
    
    map1.forEach {(k,v) -> println ("Chave: $k - Valor: $v")}
    
    println("------------------------------------")
    //Segunda maneira de criar um mapa
    val map2 = mapOf(
        "Pedro" to 2500.0,
    	"Maria" to 3000.0)
    
    map2.forEach {(k,v) -> println ("Chave: $k - Valor: $v")}

}

```


## - **Operação ou Método Coletor**
1. Usado para executar **operações** nas collections;
2. Podemos usar `forEach`, `toMap`, `toList` ou `toSet` 



---
---

**FIM DA ANOTAÇÕES**<br>
Criado por: **Guilherme Speranza**<br>
[LinkedIn - GuiSperanza](https://www.linkedin.com/in/guisperanza/)<br>
[GitHub - GuiSperanza](https://github.com/guisperanza)