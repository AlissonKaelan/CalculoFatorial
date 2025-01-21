# CalculoFatorial
 # Documentação do Projeto: ViewFatorial

## Descrição Geral

O projeto `ViewFatorial` é uma aplicação gráfica desenvolvida em Java utilizando a biblioteca Swing. O objetivo da aplicação é calcular o fatorial de um número inteiro fornecido pelo usuário através de uma interface gráfica. O fatorial é um conceito matemático que representa o produto de todos os números inteiros positivos até um determinado número.

## Estrutura da Classe

### Classe: `ViewFatorial`

- **Extensão**: `javax.swing.JFrame`
- **Responsabilidade**: Gerenciar a interface gráfica e a lógica de cálculo do fatorial.

### Construtor

```java
public ViewFatorial() {
    initComponents();
}
```

- **Descrição**: Inicializa a interface gráfica chamando o método `initComponents()`.

### Método `initComponents()`

```java
private void initComponents() {
    // Inicializa os componentes da interface gráfica
}
```

- **Descrição**: Configura todos os componentes da interface, incluindo:
  - `JSpinner` para entrada do número.
  - `JLabel` para exibir o símbolo de fatorial e o resultado.
  - `GroupLayout` para organizar os componentes na janela.

### Componentes da Interface

- **txtValor**: `JSpinner`
  - Permite ao usuário selecionar um número entre 0 e 12.
  
- **jLabel1**: `JLabel`
  - Exibe o símbolo de fatorial (!).
  
- **jLabel2**: `JLabel`
  - Exibe o símbolo de igual (=).
  
- **lblRes**: `JLabel`
  - Exibe o resultado do cálculo do fatorial.
  
- **lblDetalhes**: `JLabel`
  - Exibe os detalhes do cálculo realizado.

### Método `txtValorStateChanged(javax.swing.event.ChangeEvent evt)`

```java
private void txtValorStateChanged(javax.swing.event.ChangeEvent evt) {
    // Lógica para calcular o fatorial quando o valor do spinner muda
}
```

- **Descrição**: Este método é chamado sempre que o valor do `JSpinner` é alterado. Ele realiza as seguintes operações:
  - Obtém o valor do spinner e converte para um inteiro.
  - Calcula o fatorial do número selecionado.
  - Constrói uma string que representa a operação de cálculo.
  - Atualiza os rótulos (`lblRes` e `lblDetalhes`) com o resultado e a operação.

### Método `main(String[] args)`

```java
public static void main(String args[]) {
    // Configura o look and feel e inicia a aplicação
}
```

- **Descrição**: Método principal que configura o look and feel da aplicação e inicia a interface gráfica. Utiliza `EventQueue` para garantir que a interface seja criada na thread de eventos.

## Lógica de Cálculo do Fatorial

O cálculo do fatorial é realizado em um loop que multiplica os números inteiros de `n` até 1. O resultado é armazenado em uma variável e exibido na interface. A operação completa é apresentada em um `JLabel` para que o usuário possa ver como o resultado foi obtido.

## Considerações Finais

- **Limitações**: O cálculo do fatorial é limitado a números entre 0 e 12 devido a restrições de tamanho de inteiro.
- **Melhorias Futuras**: Poderia ser implementada uma validação de entrada e tratamento de exceções para números fora do intervalo permitido.

