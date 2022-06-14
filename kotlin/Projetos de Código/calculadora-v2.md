# CÓDIGO DE UMA VERSÃO ALTERNATIVA DA CALCULADORA EM KOTLIN

```
fun main() {
    println(" ----- PROJETO DE CALCULADORA ----- ")
        println("Digite o PRIMEIRO valor:")
    val num1 = readLine()!!.toFloat()
    
        println("Digite o SEGUNDO valor:")
    val num2 = readLine()!!.toFloat()
    
    println("""
    Escolha uma das operações abaixo: 
    Digite 1 para ADIÇÃO
    Digite 2 para SUBTRAÇÃO
    Digite 3 para MULTIPLICAÇÃO
    Digite 4 para DIVISÃO
    """)
     
 	val escolha = readLine()!!.toInt()
    
    when (escolha) {
        1 -> adicao(num1,num2)
        2 -> subtracao(num1,num2)
        3 -> multiplicacao(num1,num2)
        4 -> divisao(num1,num2)
    	else -> {
            println("Escolha uma opção válida!")
        }
    }

}

//Função SOMA
fun adicao(num1:Float, num2:Float) = println("O resultado da adição é: $[a + b]")

//Função SUBTRAÇÃO
fun subtracao(num1:Float, num2:Float) = println("O resultado da subtração é: $[a - b]")

//Função MULTIPLICAÇÃO
fun multiplicacao(num1:Float, num2:Float) = println("O resultado da multiplicação é: $[a * b]")

//Função DIVISÃO
fun divisao(num1:Float, num2:Float) = println("O resultado da divisão é: $[a / b]")


/* Criado por Gui Speranza
 * follow me at: github.com/guisperanza 
 * That's all, folks
*/
```
> O projeto ainda não está finalizado, mas quero ir deixando o código anotado por aqui.<br>
Link para o código no [Kotlin Playground](https://pl.kotl.in/QMJZvetSN)

<BR><BR><BR><BR><BR>

---
---

**FIM DA ANOTAÇÕES**<br>
Criado por: **Guilherme Speranza**<br>
[LinkedIn - GuiSperanza](https://www.linkedin.com/in/guisperanza/)<br>
[GitHub - GuiSperanza](https://github.com/guisperanza)
