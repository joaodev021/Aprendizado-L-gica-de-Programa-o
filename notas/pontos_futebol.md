### Documentação do Código: Calculando Pontuação do CDC FC

#### Objetivo do Código

Este código JavaScript calcula e exibe a pontuação do time de futebol "CDC FC" com base no número de vitórias e empates que o time teve. Além disso, compara essa pontuação com a de um time fictício chamado "Livros Velhos" para determinar se o CDC FC está indo melhor ou pior.

#### Explicação do Código

1. Função `pulaLinha()`
   - Propósito: Esta função insere uma quebra de linha (`<br>`) no documento HTML. Ela é usada para formatar a saída do texto no navegador.
   - Código:
     ```javascript
     function pulaLinha() {
         document.write("<br>");
     }
     ```

2. Função `mostra(frase)`
   - Propósito: Esta função recebe uma string (`frase`) como argumento e a exibe no documento HTML. Após exibir a frase, chama a função `pulaLinha()` para adicionar uma quebra de linha.
   - Código:
     ```javascript
     function mostra(frase) {
         document.write(frase);
         pulaLinha();
     }
     ```

3. Capturando Input do Usuário
   - Propósito: O código solicita ao usuário que insira o número de jogos que o CDC FC venceu e empatou. As entradas são obtidas através de duas janelas de prompt.
   - Detalhe Técnico: A função `prompt()` retorna uma string, então usamos `parseInt()` para converter essa string em um número inteiro.
   - Código:
     ```javascript
     var vitorias = parseInt(prompt("Quantos jogos o CDC FC venceu?"));
     var empates = parseInt(prompt("Quantos jogos o CDC FC empatou?"));
     ```

4. Calculando a Pontuação
   - Propósito: A pontuação do time é calculada com base na fórmula:
     \[
     \text{pontos} = (\text{vitorias} \times 3) + \text{empates}
     \]
     Cada vitória vale 3 pontos, e cada empate vale 1 ponto.
   - Código:
     ```javascript
     var pontos = (vitorias * 3) + empates;
     ```

5. Exibindo a Pontuação
   - Propósito: O código exibe a pontuação do time usando a função `mostra()`.
   - Código:
     ```javascript
     mostra("Nosso time tem " + pontos + " pontos!");
     ```

6. Comparação com o Time "Livros Velhos"
   - Propósito: O código compara a pontuação do CDC FC com o valor 28 (a pontuação do "Livros Velhos") e exibe uma mensagem indicando se o CDC FC está indo melhor ou pior.
   - Código:
     ```javascript
     if (pontos > 28) {
         mostra("Nosso time está indo MELHOR que o Livros velhos");
     }
     if (pontos < 28) {
         mostra("Nosso time está indo PIOR que o Livros velhos");
     }
     ```

#### Possíveis Melhorias
- Considerar o Caso de Igualdade: Atualmente, o código só compara se a pontuação é maior ou menor que 28. Seria interessante adicionar um caso onde a pontuação é igual a 28, para uma comparação mais completa.
- Uso de `console.log`: Para facilitar a depuração, o uso de `console.log` ao invés de `document.write` pode ser uma boa prática, especialmente durante o desenvolvimento.

#### Conclusão
Este código simples e eficaz permite que você pratique conceitos básicos de programação, como captura de input do usuário, funções, e lógica condicional. Ele é uma excelente introdução ao uso de JavaScript para manipular conteúdo em páginas web.
