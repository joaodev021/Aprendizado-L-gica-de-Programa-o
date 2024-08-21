## Documentação do Código

### Descrição Geral

Este código tem como objetivo calcular o número de dias que uma pessoa já viveu e quantas vezes seu coração já bateu, com base na sua idade informada pelo usuário.

### Estrutura do Código

1. Função `calculaDiasDeVida(idade)`:
    - Descrição: Esta função recebe a idade do usuário em anos e retorna o número de dias que a pessoa já viveu.
    - Parâmetros:
        - `idade` (número): A idade em anos fornecida pelo usuário.
    - Retorno: O número de dias calculado com base na idade (`idade * 365`).

    ```javascript
    function calculaDiasDeVida(idade){
      return idade * 365;
    }
    ```

2. Função `calculaBatimentos(dias)`:
    - Descrição: Esta função calcula quantas vezes o coração do usuário já bateu ao longo da vida, com base no número de dias vividos.
    - Parâmetros:
        - `dias` (número): O número de dias vividos calculado pela função `calculaDiasDeVida`.
    - Retorno: O número de batimentos cardíacos calculado como `dias * 24 * 60 * 80`. Esse cálculo assume que o coração bate 80 vezes por minuto, 24 horas por dia.

    ```javascript
    function calculaBatimentos(dias) {
      return dias * 24 * 60 * 80;
    }
    ```

3. Interação com o Usuário:
    - Coleta da Idade:
        - O código usa o método `prompt()` para pedir ao usuário que informe sua idade em anos. O valor inserido é armazenado na variável `idade`.

    - Cálculo dos Dias de Vida:
        - A idade fornecida é passada para a função `calculaDiasDeVida`, e o resultado (dias vividos) é armazenado na variável `dias`.
        - O código então exibe essa informação para o usuário usando `document.write()`.

    - Cálculo dos Batimentos Cardíacos:
        - O número de dias vividos é então passado para a função `calculaBatimentos`, e o resultado (número de batimentos cardíacos) é armazenado na variável `batimentos`.
        - Essa informação também é exibida para o usuário.

    ```javascript
    var idade = prompt("Quantos anos você tem?");
    var dias = calculaDiasDeVida(idade);
    document.write("Você já viveu " + dias + " dias de vida" + "<br>");
    var batimentos = calculaBatimentos(dias);
    document.write("Seu coração já bateu " + batimentos + " vezes. Haja coração!");
    ```

### Explicação Passo a Passo
1. Entrada de Dados: O usuário é solicitado a informar sua idade.
2. Processamento: A idade é convertida em dias de vida, e em seguida, o número de batimentos cardíacos é calculado.
3. Saída de Dados: O resultado é exibido na tela.

### Observações
- O código utiliza a função `prompt()` para entrada de dados e `document.write()` para saída. É importante notar que `prompt()` pode não funcionar em todos os contextos de um navegador, e `document.write()` pode sobrescrever o conteúdo da página se for usado após a página ser carregada.
- O cálculo de batimentos cardíacos é baseado em uma média geral de 80 batimentos por minuto, o que pode variar de pessoa para pessoa.
