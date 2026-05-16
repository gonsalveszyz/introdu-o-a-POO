# Projeto de Estudos: Classe Filme em Java

Este projeto foi desenvolvido com finalidade de estudo, com o objetivo de praticar conceitos iniciais de **Java** e **Programação Orientada a Objetos**, também conhecida como **POO**.

O código simula a criação de uma classe chamada `Filme`, que representa um filme com seus principais atributos e alguns comportamentos básicos, como exibir sua ficha técnica, receber avaliações e calcular a média das notas.

---

## Objetivo do Projeto

O objetivo principal deste projeto é estudar e praticar conceitos fundamentais de Java, como:

- Criação de classes;
- Criação de objetos;
- Atributos;
- Métodos;
- Parâmetros;
- Retorno de valores;
- Operadores de atribuição;
- Incremento de variáveis;
- Cálculo de média;
- Uso do método `main`;
- Conceitos básicos de Programação Orientada a Objetos.

Este projeto não tem finalidade comercial. Ele foi criado apenas para fins de aprendizado.

---

## Estrutura do Projeto

O projeto possui duas classes principais:

## Código da classe Filme
```text
public class Filme {
    String nome;
    int anoDeLancamento;
    boolean incluidoNoPlano;
    double somaDasAvaliacoes;
    int totalDeAvaliacoes;
    int duracaoEmMinutos;

    void exibeFichaTecnica() {
        System.out.println("Nome do Filme: " + nome);
        System.out.println("Ano de Lançamento: " + anoDeLancamento);
    }

    void avalia(double nota) {
        somaDasAvaliacoes += nota;
        totalDeAvaliacoes++;
    }

    double pegaMedia() {
        return somaDasAvaliacoes / totalDeAvaliacoes;
    }
}
```

## Código da classe Principal

```java
public class Principal {
    public static void main(String[] args) {
        Filme meuFilme = new Filme();

        meuFilme.nome = "Poderoso chefao";
        meuFilme.anoDeLancamento = 1970;
        meuFilme.duracaoEmMinutos = 180;

        meuFilme.exibeFichaTecnica();

        meuFilme.avalia(8);
        meuFilme.avalia(5);
        meuFilme.avalia(10);

        System.out.println(meuFilme.somaDasAvaliacoes);
        System.out.println(meuFilme.totalDeAvaliacoes);
        System.out.println(meuFilme.pegaMedia());
    }
}
```
