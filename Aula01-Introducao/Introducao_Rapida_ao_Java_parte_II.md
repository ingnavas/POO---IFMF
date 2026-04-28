## AULA 02 - JAVA

---
**☕ Java é considerada uma linguagem compilada porque o código fonte (.java) é transformado antes de executar.
O compilador javac converte o código em bytecode (.class).
Esse bytecode não roda direto no sistema operacional.
Ele é executado pela Java Virtual Machine (JVM).
Assim, o mesmo programa pode rodar em diferentes sistemas sem alteração.**

⚠️ Desabilite a função autocompleta


O primeiro programa a ser escrito no Java é:

```java
public class Caminhao {
    public static void main(String[] args){
        System.out.println("Vamos arrumar a nossa mina");       
    }

}
```

inicialmente vamos focar na lógica do programa que no caso anterior é 

```java
System.out.println("Vamos arrumar a nossa mina");
```

A sintaxe da classe posterioremente estaremos aprendedo na medida das explicações e uso. Inicialmente esta será usada de forma padrão como

```java
public class Caminhao {
    public static void main(String[] args){

   //AQUI COLOCAREMOS O NOSSO CÓDIGO
      
    }

}
```

Forçe alguns erros de sintaxe para verificar as informações que programa retorna
- Elimine o ";";
- Elimine o "void" na declaração da classe;
- Use a palavra "String" no plural, isto é "Strings".

Em cada caso avalie o erro obtido no terminal.

⚠️ Dependendo da IDE (Integrated Development Environment = Ambiente de Desenvolvimento Integrado) o erro pode ser indicado com maior precisão)

---

### 📝 Definição de variáveis

Realize uma definição de programa que contenha

- Uma variável que indique a capacidade de carga por ciclo das escavadeiras A e B, sendo uma *inteiro* e outra *double*;
- Uma variável que indique a identificação das escavadeira A e B como un texto con tres letras e tres numeros;
- Uma variável que indique o tempo de carregamento das escavadeiras a e B;
- Uma variável que defina o status da escavadeira que pode ser: Desligada, Partindo (startup), Operando, em manutenção;
- Imprima os resultados na tela, use texto antes de cada valor.

Faça algumas alterações para gerar erros de forma proposital e verique os erros gerados. 

<details>
 
  <summary><b>🔽Ver código / 🔼 Ocultar código</b></summary>
 
```java
public class Veiculo {
    public static void main(String[] args){
        System.out.println("Vamos arrumar a nossa mina"); 
        
        int     capacidadeCargaEscavadeiraA     = 100;
        System.out.println("A capacidade de carga da escavadeira 'A' é:"+capacidadeCargaEscavadeiraA+" toneladas");
        
        double  capacidadeCargaEscavadeiraB     = 100;
        System.out.println("A capacidade de carga da escavadeira 'B' é:"+capacidadeCargaEscavadeiraB+" toneladas"); 
        
        
        String  idFlotaMinaEscavadeiraA = "MOP-212";
        System.out.println("A identificação da escavadeira 'A' é:"+ idFlotaMinaEscavadeiraA);
        String  idFlotaMinaEscavadeiraB = "MOP-214";
        System.out.println("A identificação da escavadeira 'B' é:"+ idFlotaMinaEscavadeiraB);
       
        int     tempoCarregamentoEscavadeiraA   = 23;
        System.out.println("O tempo para carga da escavadeira é:"+ tempoCarregamentoEscavadeiraA+ " min");
       
        int     tempoCarregamentoEscavadeiraB   = 32;
        System.out.println("O tempo para carga da escavadeira é:"+ tempoCarregamentoEscavadeiraB+ " min");
       
        double cargaTotal= capacidadeCargaEscavadeiraA+capacidadeCargaEscavadeiraB;
        System.out.println("A capacidade de carga da planta é:"+cargaTotal+" toneladas");
    
        String[] estatus={"Desligada", "Partindo (startup)", "Operando", "em manutenção"};

        System.out.println("Os estados são: " + estatus);
        System.out.println("Os estados são: "+estatus[0]+";"+estatus[1]+";"+estatus[2]+";"+estatus[3]);
   
    }

}  
```
</details> 

---

### ➰ Loops de controle

Os ciclos de controle (loops) são usados para repetir um bloco de código várias vezes, evitando repetição manual. 
Os Loops permitem automatizar tarefas repetitivas, como:

- Processar listas
- Simular operações (ex: ciclos de uma máquina)
- Validar dados

*1. for*

Usado quando você sabe quantas vezes quer repetir. Ex: percorrer um array, contar de 1 a 10

```Java
for (inicializacao; condicao; incremento) {
    // bloco de código
}
```

- Inicializacao: executa uma vez (ex: int i = 0)
- Condicao: enquanto for verdadeira, continua
- Incremento: atualização a cada repetição (ex: i++)

<details>
 
  <summary><b>🔽Ver código / 🔼 Ocultar código</b></summary>
 
```java
public class Ciclos {
    public static void main(String[] args){
        
        int[] cargas = {50, 60, 70};

        for (int i = 0; i < cargas.length; i++) {
            System.out.println("Carga do caminhão " + i + ": " + cargas[i]);
        }

    }
}
```

</details> 

*2. while*

Usado quando a repetição depende de uma condição. Repete enquanto a condição for verdadeira

```java
while (condicao) {
    // bloco de código
}
```
- Testa a condição antes de executar
- Pode não executar nenhuma vez

<details>
 
  <summary><b>🔽Ver código / 🔼 Ocultar código</b></summary>
 
```java
public class Ciclos {
    public static void main(String[] args){
       int cargaAtual = 0;
        while (cargaAtual < 100) {
            cargaAtual += 20;
            System.out.println("Carregando... " + cargaAtual);
        }

    }
}

```

</details> 

*3. do-while*

Parecido com o while, mas executa pelo menos uma vez, mesmo que a condição seja falsa.

```java
do {
    // bloco de código
} while (condicao);
```
- Executa primeiro
- Testa a condição depois
- Sempre executa pelo menos uma vez

<details>
 
  <summary><b>🔽Ver código / 🔼 Ocultar código</b></summary>
 
```java
public class Ciclos {
    public static void main(String[] args){
        int tentativas = 0;

        do {
            System.out.println("Tentando ligar a britadeira...");
            tentativas++;
        } while (tentativas < 3);

    }
}
```

</details> 

---

### ➰ Estruturas de decisão

As estruturas de decisão são mecanismos que permitem ao programa tomar decisões durante sua execução. Com base em condições (verdadeiras ou falsas), o código pode seguir diferentes caminhos, executando apenas as instruções apropriadas para cada situação. Essas estruturas são fundamentais para tornar os programas dinâmicos e adaptáveis a diferentes cenários. Entre as principais estão o if, if-else, if-else if e o switch, cada uma indicada para tipos específicos de decisão

*1. if

Executa o bloco somente se a condição for verdadeira

```java
if (condicao) {
    // bloco de código
}
```
<details>
 
  <summary><b>🔽Ver código / 🔼 Ocultar código</b></summary>
 
```java
if (carga > 100) {
    System.out.println("Caminhão carregado");
}
```

</details> 

*2. if - else

Escolhe entre dois caminhos

```java
if (condicao) {
    // verdadeiro
} else {
    // falso
}
```
<details>
 
  <summary><b>🔽Ver código / 🔼 Ocultar código</b></summary>
 
```java
boolean operando = false;

if (operando) {
    System.out.println("Britadeira em operação");
} else {
    System.out.println("Britadeira parada");
}
```

</details> 

*3. if - else if - else

Permite várias condições em sequência

```java
if (condicao1) {
    // bloco 1
} else if (condicao2) {
    // bloco 2
} else {
    // nenhum caso anterior
}
```
<details>
 
  <summary><b>🔽Ver código / 🔼 Ocultar código</b></summary>
 
```java
int carga = 70;

if (carga < 50) {
    System.out.println("Carga baixa");
} else if (carga < 100) {
    System.out.println("Carga média");
} else {
    System.out.println("Carga alta");
}
```

</details> 

*4. switch-case

Compara o valor de uma variável com várias opções possíveis e executar o bloco correspondente.


```java
switch (variavel) {
    case valor1:
        // código
        break;
    case valor2:
        // código
        break;
    default:
        // padrão
}
```
- switch → avalia uma variável
- case → compara valores
- break → evita executar os próximos casos
- default → executa se nenhum caso for atendido

<details>
 
  <summary><b>🔽Ver código / 🔼 Ocultar código</b></summary>
 
```java
switch (status) {
    case 1:
        System.out.println("Desligada");
        break;
    case 2:
        System.out.println("Operando");
        break;
    case 3:
        System.out.println("Em manutenção");
        break;
    default:
        System.out.println("Status desconhecido");
}
```

</details> 

⚠️ Precaução com a obrigatoriedade do  *break*
O break interrompe o switch após executar um caso. Sem break, ocorre o chamado *fall-through*, ou seja, os próximos casos também serão executados.





