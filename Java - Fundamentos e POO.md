# ☕ Java: Da Sintaxe aos Pilares da Orientação a Objetos 

## 🎯 Objetivo Dominar o ambiente de execução Java (JRE/JDK), a sintaxe básica da linguagem, o fluxo de controle e os conceitos fundamentais da Programação Orientada a Objetos (POO).

--- 

## 💻 Módulo 1: O Primeiro Código (JRE e JDK) 

### ⚙️ O Ambiente Java 

- **JRE (Java Runtime Environment):** O ambiente necessário para *executar* programas Java. Contém a JVM e as bibliotecas essenciais. 
- **JDK (Java Development Kit):** O kit completo para *desenvolver* e *executar* programas Java. Inclui o JRE + ferramentas de desenvolvimento (compilador, debugger, etc.). 
- **JVM (Java Virtual Machine):** A máquina virtual que executa o bytecode (código compilado) do Java, garantindo a portabilidade da linguagem (Write Once, Run Anywhere). 

### 📝 Estrutura Básica do Código 

- **`public class NomeDaClasse`**: Ponto de partida do programa (o arquivo deve ter o mesmo nome). 
- **`public static void main(String[] args)`**: O método principal (Main) por onde a execução do programa começa. 
- **`System.out.println()`**: Comando para imprimir texto no console. 

### 🔢 Variáveis e Tipos Primitivos 

- **Tipos Mais Comuns:** `int`, `double`, `boolean`, `char`. 
- **Declaração:** `tipo nomeVariavel = valor;` 
- **Casting (Conversão):** Conversão explícita de um tipo para outro (ex: `(int) valorDouble`). 

### ➡️ Fluxo de Controle 

- **Condicionais:** `if`, `else`, `else if`. 
- **Laços (Loops):** 
- `while`: Executa enquanto uma condição for verdadeira. 
    - `for`: Executa um número definido de vezes. 
- **`switch/case`**: Estrutura de múltipla escolha. 

--- 

## 🧱 Módulo 2: Java OO (Orientação a Objetos) 

### 🌟 Conceitos Fundamentais de POO 

- **Objeto:** Uma instância de uma classe. É a representação de algo do mundo real (ex: um `Cliente`, uma `Conta`). 
- **Classe:** O "molde" ou "planta" para criar objetos. Define os atributos e os comportamentos. 

### 🔑 Atributos e Métodos 

- **Atributos (Campos/Variáveis de Instância):** As características de um objeto (ex: `saldo`, `titular`). 
- **Métodos (Comportamentos):** As ações que um objeto pode realizar (ex: `depositar()`, `sacar()`). 

### 🏗️ Construtores 

- **Função:** Método especial usado para criar (instanciar) um objeto. 
- **Regra:** Geralmente possui o mesmo nome da classe. 
- **Construtor Padrão:** O Java fornece um construtor sem argumentos por padrão se nenhum for declarado. - **Palavra-chave `this`:** Usada para referenciar os atributos da própria instância (objeto). 

### 🤫 Encapsulamento 

- **Conceito:** Esconder os detalhes internos de um objeto e proteger seus dados. 
- **`private`**: Modificador de acesso que impede o acesso direto ao atributo. 
- **Getters e Setters:** Métodos públicos usados para **obter** (`get`) e **modificar** (`set`) atributos privados de forma controlada. 

### 🧩 Pilares da POO (Aprofundamento) 

*Embora o curso inicial de POO foque em Classes e Encapsulamento, os próximos geralmente cobrem:* 

1. **Herança:** Permite que uma classe herde atributos e métodos de outra classe (reaproveitamento de código). 
    * **Palavra-chave:** `extends`. 
2. **Polimorfismo:** Capacidade de um objeto assumir diferentes formas (métodos com o mesmo nome que se comportam de maneira diferente dependendo do objeto). 
3. **Abstração:** Focar nos detalhes essenciais (o que o objeto faz) e esconder os detalhes irrelevantes (como ele faz). 