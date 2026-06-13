# Exercícios Java-Júnior

- Faça um programa que mostre a mensagem "Alô mundo" na tela.

**Resolução:**

<details>
  <summary>Spoiler warning</summary>

```java
System.out.print("Alô mundo");
```
</details>

* * *

- Faça um programa que exibe uma frase concatenada com a idade e o nome de um usuário (variáveis declaradas).

**Resolução:**

<details>
  <summary>Spoiler warning</summary>

```java
public static void main(String[] args) {
    int idade_do_usuario = 20;
    String nomeDoUsuario = "João";

    // Printando as variáveis declaradas
    System.out.print("Olá, meu nome é ");
    System.out.print(nomeDoUsuario);
    System.out.print(" e minha idade é ");
    System.out.print(idade_do_usuario);
    System.out.println(" anos");

    // Printando de forma concatenada as variáveis declaradas
    System.out.print("Olá, meu nome é " + nomeDoUsuario + " a minha idade é " + idade_do_usuario);
}
```
</details>

* * *

- Faça um programa que exibe a soma e a substração de 2 números (variáveis declaradas).

**Resolução:**

<details>
  <summary>Spoiler warning</summary>

```java
public static void main(String[] args) {
    // Armazenar os valores em memória
    int numero1 = 20;
    int numero2 = 20;

    // Criando a operação de soma
    int resultadoDaSoma = numero1 + numero2;

    // Criando a operação de subtração
    int resultadoDaSubtracao = numero1 - numero2;

    // Exibindo a operação de soma para o usuário
    System.out.println("O resultado da soma é: "+resultadoDaSoma);

    // Exibindo a operação de subtração para o usuário
    System.out.println("O resultado da subtração é: "+resultadoDaSubtracao);

}
```
</details>

* * *

- Faça um programa que receba 4 notas bimestrais e mostre a média aritmética.

**Resolução:**

<details>
  <summary>Spoiler warning</summary>

```java
public class MediaBimestral {
    
    public static void main(String[] args) {
        
        Scanner scanner = new Scanner(System.in);
        
        System.out.println("=== Cálculo de Média Bimestral ===\n");
        
        System.out.print("Digite a 1ª nota: ");
        double nota1 = scanner.nextDouble();
        
        System.out.print("Digite a 2ª nota: ");
        double nota2 = scanner.nextDouble();
        
        System.out.print("Digite a 3ª nota: ");
        double nota3 = scanner.nextDouble();
        
        System.out.print("Digite a 4ª nota: ");
        double nota4 = scanner.nextDouble();
        
        // Cálculo da média
        double media = (nota1 + nota2 + nota3 + nota4) / 4;
        
        System.out.println("\n=================================");
        System.out.printf("A média aritmética é: %.2f%n", media);
        System.out.println("=================================");
        
        scanner.close();
    }
}
```
</details>

* * *

- Faça um programa que converta metros para centímetros.

**Resolução:**

<details>
  <summary>Spoiler warning</summary>
  
```java
public class ConversorMetrosCentimetros {
    
    public static void main(String[] args) {
        
        Scanner scanner = new Scanner(System.in);
        
        System.out.println("=== Conversor de Metros para Centímetros ===\n");
        
        System.out.print("Digite a quantidade de metros: ");
        double metros = scanner.nextDouble();
        
        // Conversão
        double centimetros = metros * 100;
        
        System.out.println("\n=================================");
        System.out.printf("%.2f metro(s) = %.2f centímetro(s)%n", metros, centimetros);
        System.out.println("=================================");
        
        scanner.close();
    }
}
```
</details>

* * *

- Faça um Programa que recebe o quanto você ganha por hora e o número de
horas trabalhadas no mês. Calcule e mostre o total do seu salário no referido mês.

**Resolução:**

<details>
  <summary>Spoiler warning</summary>

```java
public static void main(String[] args) {
    // Armazenou os dois dados necessários para o processamento
    float qtdDeHorasTrabalhadas = 10;
    float salarioPorHora = 20;

    // Calcular o salário bruto
    float salarioBruto = qtdDeHorasTrabalhadas * salarioPorHora;

    System.out.println("Você trabalhou " +qtdDeHorasTrabalhadas
            + "Hrs, e você recebe R$" +salarioPorHora
            + " por hora");

    System.out.println("Portanto, seu salário este mês, será: R$"+salarioBruto);
}
```
</details>

* * *

- Faça um programa que peça a temperatura em graus Fahrenheit, transforme e
mostre a temperatura em graus Celsius.

**Resolução:**

<details>
  <summary>Spoiler warning</summary>
  
```java
public class ConversorTemperatura {
    
    public static void main(String[] args) {
        
        Scanner scanner = new Scanner(System.in);
        
        System.out.println("=== Conversor de Fahrenheit para Celsius ===\n");
        
        System.out.print("Digite a temperatura em graus Fahrenheit (°F): ");
        double fahrenheit = scanner.nextDouble();
        
        // Fórmula de conversão: C = (F - 32) * 5 / 9
        double celsius = (fahrenheit - 32) * 5.0 / 9.0;
        
        System.out.println("\n=================================");
        System.out.printf("%.2f °F = %.2f °C%n", fahrenheit, celsius);
        System.out.println("=================================");
        
        scanner.close();
    }
}
```
</details>

* * *

- Faça um Programa que receba o quanto você ganha por hora e o número de
horas trabalhadas no mês. Calcule e mostre o total do seu salário no referido
mês, sabendo-se que são descontados 11% para o Imposto de Renda, 8% para o
INSS e 5% para o sindicato, faça um programa que nos dê respectivamente:
  - Salário bruto.
  - Quanto pagou ao INSS.
  - Quanto pagou ao sindicato.
  - Qual o salário líquido do funcionário.

**Resolução:**

<details>
  <summary>Spoiler warning</summary>

```java
public static void main(String[] args) {
        Scanner leitor = new Scanner(System.in);
        double impostoDeRenda;
        double inss;
        double sindicato;
        double salarioLiquido;

        //Dados do salario BRuto
        System.out.println("Por favor digite seu salario por horas: ");
        double salarioPorHora = leitor.nextDouble();
        System.out.println("Por favor digite as horas trbalhadas: ");
        double horasTrabalhadas = leitor.nextDouble();

        //calculo de Salario Bruto
        double salarioBruto = salarioPorHora * horasTrabalhadas;

        //calcular descontos
        impostoDeRenda = salarioBruto * 0.11;
        inss = salarioBruto * 0.08;
        sindicato = salarioBruto * 0.05;
        double descontos = impostoDeRenda + inss + sindicato;

        //calcular salario liquido
        salarioLiquido = salarioBruto - descontos;

        //Folha de Pagamento
        System.out.println("===============================================");
        System.out.println("                    Pagamento                  ");
        System.out.println("===============================================");
        System.out.println("Salario por hora: \t\t" + salarioPorHora);
        System.out.println("Horas trabalhadas: \t\t" + horasTrabalhadas);
        System.out.println("SALARIO BRUTO: \t\t" + salarioBruto);
        System.out.println("===============================================");
        System.out.println("DESCONTOS:");
        System.out.println("Imposto de Renda (11%): \t" + impostoDeRenda);
        System.out.println("INSS (8%): \t\t\t" + inss);
        System.out.println("Sindicato (5%): \t\t" + sindicato);
        System.out.println("TOTAL DESCONTOS: \t\t" + descontos);
        System.out.println("===============================================");
        System.out.println("SALARIO LIQUIDO: \t\t" + salarioLiquido);
        System.out.println("===============================================");
        }
}
```
</details>
