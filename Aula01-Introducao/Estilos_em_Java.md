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

**3. ➿Estruturas de controle

```java
if (condicao) {
    // executa se verdadeiro
}
```

Toda e qualquer informação que fica dentro das chaves pertence à estrutura de controle

⚠️ Como recomendação de boa prática de programação, sempre deve-se usar chaves, mesmo quando não seja obrigatório

| ❌ Evite usar | ✅ Melhor use |
|--------------|-------------|
|if (condicao)
    executar();
    |if (condicao) {
    executar();
}|

O anterior evita erros no futuro, posto que se o código dentro da condição aumenta, não haverá erro de compilação. 







