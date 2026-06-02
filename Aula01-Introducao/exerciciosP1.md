## EXEMPLOS DE TRABALHO 

Questão 1

Escreva uma classe cujos objetos representam alunos matriculados em uma disciplina. Cada objeto dessa classe deve guardar os seguintes dados do aluno: matrícula, nome, 2 notas de prova e 1 nota de trabalho. Escreva os seguintes métodos para esta classe:

| Método | Descrição |
|---------|-----------|
| `media()` | Calcula a média final do aluno (cada prova tem peso 2,5 e o trabalho tem peso 2). |
| `final()` | Calcula quanto o aluno precisa para a prova final (retorna zero se ele não for para a final). |

```java
public class Alunos {
    //ATRIBUTOS
    private String nomeAluno;
    private int matriculaAluno;
    private double notaP1;
    private double notaP2;
    private double notaPF;
    private double notaT1;
    private double media;
    

    //CONSTRUTORES
    Alunos (){
    }

    Alunos (String nomeAluno){
        this.nomeAluno=nomeAluno;
    }

    Alunos (String nomeAluno, int matriculaAluno){
        this.nomeAluno=nomeAluno;
        this.matriculaAluno = matriculaAluno;
    }

    //METODOS DE ACESSO
    public void setNomeAluno(String nomeAluno){
        this.nomeAluno=nomeAluno;
    }

    public String getNomeAluno(){
        return this.nomeAluno;
    }

    public void setMatriculaAluno(int matriculaAluno){
        this.matriculaAluno=matriculaAluno;
    }

    public int getMatriculaAluno(){
        return this.matriculaAluno;
    }

    public void setNotaP1(double notaP1){
        this.notaP1 = notaP1;
    }

    public double getNotaP1(){
        return this.notaP1;
    }

    public void setNotaP2(double notaP2){
        this.notaP1 = notaP2;
    }

    public double getNotaP2(){
        return this.notaP2;
    }

    public void setNotaT1(double notaT1){
        this.notaT1 = notaT1;
    }

    public double getNotaT1(){
        return this.notaT1;
    }

    public void setNotaPF(double notaPF){
        this.notaPF = notaPF;
    }

    public double getNotaPF(){
        return this.notaPF;
    }

    public double getMedia(){
        return this.media;
    }

    //METODOS DE ROTINAS

    public double media(){
        double notaMedia = (this.notaP1*2.5+this.notaP2*2.5+
            this.notaT1*2)/7;
        return notaMedia;
    }

    public double calculeNotaFinalNecesaria(){
        if (this.media>=60){
            this.notaPF=this.media;
            return 0; 
        }
        else{
            this.notaPF = (60-this.media*7)/3;
            return notaPF;
        }
    }

}

```

A classe anterior é chamada por

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
       
        Scanner teclado = new Scanner(System.in);
        Alunos aluno= new Alunos();
        int matricula=0;

        System.out.print("Digite o nome do aluno: ");
        //String nomeAluno = teclado.nextLine();
        aluno.setNomeAluno(teclado.nextLine());

        System.out.print("Digite a matricula : ");
        if (teclado.hasNextInt()) {
            matricula = teclado.nextInt();
            teclado.nextLine();
        } else {
            System.out.println("Valor inválido!");
            matricula=-1;
        }

        aluno.setMatriculaAluno(matricula);
       

        System.out.println("Aluno cadastrado: " + aluno.getNomeAluno()
    + " /com matricula numero: " + String.valueOf(aluno.getMatriculaAluno()) );

        teclado.close();
        
    }

}

```

