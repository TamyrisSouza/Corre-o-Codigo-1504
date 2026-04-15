# Corre-o-Codigo-1504
Correção de código.

Funcionário:
Chaves em locais errados do código 
Classe e Nome estavam declarados como Double
Percentual estava declarado como texto no return
Construtor errado (tem void)



Gerente:
Variável Salário não foi declarada
Variáveis declaradas dentro dos parenteses do return
Não foi  declarada extensão de Funcionário para Gerente
BônusExtra estava declarado como texto

Main:
Salário estava como texto
Gerente estava declarado como funcionário 
Não possui o cálculo de bônus

Main 
package org.senai.exemplos;


public class Main {
    public static void main(String[] args) {
        Funcionario func1 = new Funcionario("Priscila", 1000);
        func1.mostrarDados();

        Gerente func2 = new Gerente();
        System.out.println("Bônus: " + func2.calcularBonus(1.0));

    }
}

Funcionarios
package org.senai.exemplos;


public  class Funcionario {
    protected String nome;
    protected double salario;
    protected double percentual;

    public Funcionario(String nome, double salario) {
        this.nome = nome;
        this.salario = salario;
    }

    public double calcularBonus(double percentual) {
        this.percentual = percentual;
        return salario * percentual;
    }

    public void mostrarDados() {

        System.out.println("Nome: " + nome + " | Salário: " + salario + "Bônus: " + );
    }
}

Gerente
package org.senai.exemplos;

public class Gerente{
    private double bonusExtra;
    private double percentual;
    private double salario;
    private String nome;

    public double calcularBonus(double percentual) {
        this.percentual = percentual;
        // ERRO: variável não existe
        return salario * percentual;
    }

    public void mostrarBonus() {

        System.out.println("Bônus extra: " + bonusExtra);
    }
}
