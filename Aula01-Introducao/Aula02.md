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




