# 📘 ESTILOS EM JAVA

---

## ☑️ Uso de camelCase e PascalCase

Java segue convenções de nomenclatura que ajudam na leitura e organização do código. É usado o padrão **🐪 camelCase** para variáveis e métodos, por exemplo:

- marcaCaminhao  
- capacidadeBritaderia  
- velocidadeMaxima  

Já para classe é usado o padrão **🔺PascalCase**, por exemplo:

- Caminhao  
- Escavadeira  
- OperadorBritadeira  
- SistemaMina  

⚠️ Na elaboração de um programa use nomes que sejam totalmente descritivos e tenham relação direta com o contexto do programa elaborado e por tanto evite nomes genéricos, por exemplo


| ❌ Não use | ✅ Melhor use            |
|-----------|------------------------|
| x         | capacidadeBritaderia   |
| mC        | marcaCaminhao          |
| velMax    | velocidadeMaxima       |

---

## ☑️ Uso de colchetes, chaves e parênteses

Deve-se fazer uso correto dos símbolos **( )**, **{ }** e **[ ]**. Estes não são apenas detalhes de sintaxe, sendo que definem a estrutura, organização e funcionamento do programa.

---
Os parênteses são usados principalmente para:

**1. ☎️ Chamada de métodos**

Sempre que um método é chamado, usamos parênteses:

```java
System.out.println("Exemplo mineração");
```

e, mesmo quando não há parâmetros, os parênteses são obrigatórios:

```java
metodo();
```

**2. 📝 Definição de métodos**

Na declaração de métodos, os parênteses indicam os parâmetros:

```java
void carregarCaminhao(int quantidade)
```

Observe que o parâmetro definido como inteiro **int** quantidade está dentro dos parênteses.

**3. ➿Estruturas de controle**

Parênteses também aparecem em estruturas como:

```java
if (condicao) {
}
while (condicao) {
}
```

Eles definem a condição que será avaliada.

**4. ➕✖️ Expressões matemáticas**

Servem para controlar a ordem de execução:

```java
int resultado = (a + b) * c;
```

Sem parênteses, o resultado seria diferente.

---
As chaves são usadas para definir blocos de código, agrupando instruções que pertencem ao mesmo contexto

**1. 📚 Blocos de classes**

```java
public class Caminhao {
   // código da classe aqui
}
```

Toda e qualquer informação que fica dentro das chaves pertence à classe.

**2. 🛠️ Blocos de métodos**

```java
void carregar() {
    // código aqui
}
```

Toda e qualquer informação que fica dentro das chaves pertence ao método.

**3. ➿Estruturas de controle**

```java
if (condicao) {
    // executa se verdadeiro
}
```

Toda e qualquer informação que fica dentro das chaves pertence à estrutura de controle

⚠️ Como recomendação de boa prática de programação sempre devem-se usar chaves, mesmo quando não seja obrigatório

| ❌ Evite usar | ✅ Melhor use |
|--------------|-------------|
| if (condicao)<br>executar(); | if (condicao) {<br>executar();<br>} |

O anterior evita erros no futuro, posto que se o código dentro da condição aumenta, não haverá erro de compilação. 

---

Os colchetes são usados principalmente para trabalhar com arrays (vetores).

Declaração de arrays (os arrays devem ter elementos do mesmo tipo)

**1. 🔰 Inicialização**

```java
int[] aberturaBritadeira= {20, 40, 60, 75};
```

**2. 🚪 Acesso a elementos (nos arrays para o acesso de elementos o índice começa em zero)**

```java
aberturaBritadeira[0];
aberturaBritadeira[1];
```

Os símbolos **( )**, **{ }** e **[ ]** são essenciais para estruturar programas em Java. Eles definem:

**como métodos são chamados e definidos**

**como blocos de código são organizados**

**como coleções de dados são manipuladas**

Desta forma, ⚠️ erros nesses símbolos podem causar falhas no programa ou comportamentos inesperados e, por tanto, dominar o uso correto deles é um passo fundamental para escrever código claro, organizado e funcional!

---

## ☑️ Tipos Primitivos

Variáveis do tipo primitivo no Java são aquelas variáveis cujo valor que elas guardam é o real conteúdo da variável. Neste caso, quando for usado o operador de atribuição *=* o valor real da variável será o valor copiado. A tabela na sequência apresenta os tipos primitivos possíveis no Java.

| Tipo    | Descrição                          | Exemplo            | Tamanho |
|--------|----------------------------------|--------------------|--------|
| boolean | Verdadeiro ou Falso              | true, false        | ~1 bit |
| byte    | Número inteiro pequeno           | 10, -5             | 1 byte |
| short   | Número inteiro médio             | 1000, -2000        | 2 bytes |
| char    | Caractere Unicode                | 'A', 'c'           | 2 bytes |
| int     | Número inteiro                   | 10, 20             | 4 bytes |
| float   | Número decimal (precisão simples)| 3.14f, 2.5f        | 4 bytes |
| long    | Número inteiro grande            | 100000L            | 8 bytes |
| double  | Número decimal (precisão dupla)  | 3.14, 22.998       | 8 bytes |

Na boa prática de programação, use *int* como padrão para inteiro e *double* como padrão para decimal.

**1. 🟰 Declaração de uma variável**

A ação de declarar uma variável no Java implica definir seu tipo, o seu nome y de forma opcional inicializar o seu valor .

**tipo nome;**

ou

**tipo nome = valor;**

Por exemplo,

```java
int capacidade = 100;
double velocidade = 45.5;
boolean ligado = true;
char tipo = 'A’;
```

Nas boas práticas de programação devemos declarar uma variável por linha e inicializar seu valor sempre que for possível. 

---
☑️ String

Em Java, *String* não é do tipo primitivo, é uma classe. Mesmo assim é usada o tempo tudo

Por ser uma classe, como vai ser visto posteriormente, deve ser declarada como 

```java
String nome = new String("Caminhão fora de estrada 01");
```

porém ela é considerada um caso especial em função de seu uso contínuo e pode ser declarada de forma similar a um tipo primitivo, por exemplo:

```java
String nome = "Caminhão fora de estrada 01 "; 
```

ou até ser declarada sem ser inicializada

```java
String nome;  
```
 e ser inicializada depois.
 
```java
String nome;
//...outro trecho de código...
nome = "Caminhão fora de estrada 01"; 
```



