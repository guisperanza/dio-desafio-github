# COLEÇÕES, ARRAYS, LIST, SET and MAP

### **MENU DE CONTEÚDOS**
- [**CONCEITOS SOBRE COLEÇÕES**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--conceitos-sobre-cole%C3%A7%C3%B5es)<br> 
    -> [**Como Criar uma Coleção**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--como-criar-cole%C3%A7%C3%B5es)
- [**ARRAY**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--array)<br> 
    -> [**IntArray/intArrayOf**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--intarrayof)<br>
    -> [**Array/arrayOf**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--array-de-string)<br>
    -> [**DoubleArray/doubleArrayOf**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--double-array)<br>
- [**OPERAÇÕES COM ARRAY**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--opera%C3%A7%C3%B5es-com-array)<br>
    -> [**SORT**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--sort)<br>
    -> [**MAX, MIN e AVERAGE**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--max-min-e-average)<br>
    -> [**FILTER**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--filter)<br>
    -> [**ARRAY COUNT, FIND e ANY**](https://github.com/guisperanza/dio-desafio-github/blob/main/kotlin/colecos-arrays-listas.md#--array-count-find-e-any)<br>
- [**PRÓXIMO TÓPICO**]()

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

### - **MAX, MIN e AVERAGE**
``` 
fun main() {
    val barra:String = "------------------"
    val salarios = doubleArrayOf(1000.0, 3000.0, 500.0)
  
    for (salario in salarios){
        println(salario)
    }
    
    println(barra)
    
    println("O maior salário é: R$ ${salarios.max()}") //Retorna o maior valor da array
    println("O menor salário é: R$ ${salarios.min()}") //Retorna o menor valor da array
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

---
---

**FIM DA ANOTAÇÕES**<br>
Criado por: **Guilherme Speranza**<br>
[LinkedIn - GuiSperanza](https://www.linkedin.com/in/guisperanza/)<br>
[GitHub - GuiSperanza](https://github.com/guisperanza)