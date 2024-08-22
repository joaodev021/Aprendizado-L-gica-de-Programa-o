```markdown
# Documentação: Cálculo de Pontos em Jogos de Futebol

Este script em JavaScript calcula e compara os pontos de dois times de futebol (NJ e CDF FC) com base no número de vitórias e empates de cada time. O objetivo é determinar qual time está se saindo melhor, pior ou se estão empatados em termos de pontos.

## Estrutura do Código

### 1. Função `calculaPontos(vitorias, empates)`

**Descrição:**
Esta função recebe o número de vitórias e empates como parâmetros e retorna o total de pontos do time.

**Fórmula usada:**  
- Cada vitória vale 3 pontos.
- Cada empate vale 1 ponto.

**Código:**
```javascript
function calculaPontos(vitorias, empates) {
  return (vitorias * 3) + empates;
}
```

**Exemplo de uso:*
Se um time tem 4 vitórias e 2 empates, a função calculará os pontos como:
\[ \text{Pontos} = (4 \times 3) + 2 = 14 \text{ pontos} \]

### 2. Função `pulaLinha()`

**Descrição:**  
Esta função insere uma quebra de linha na página HTML, facilitando a organização do texto exibido.

**Código:**
```javascript
function pulaLinha() {
  document.write("<br>");
}
```

### 3. Função `mostra(frase)`

**Descrição:**  
Esta função recebe uma frase como parâmetro e a exibe na página HTML.

**Código:**
```javascript
function mostra(frase) {
  document.write(frase);
}
```

### 4. Interação com o Usuário

O código solicita ao usuário, por meio de caixas de diálogo (`prompt`), o número de vitórias e empates de dois times: NJ e CDF FC. Esses valores são convertidos de texto para número inteiro usando `parseInt`.

**Código:**
```javascript
var vitoriasNJ = parseInt(prompt("Quantos jogos o NJ venceu?"));
var empatesNJ = parseInt(prompt("Quantos jogos o NJ empatou?"));
var pontosNJ = calculaPontos(vitoriasNJ, empatesNJ);

var vitoriasCDF = parseInt(prompt("Quantos jogos o CDF FC venceu?"));
var empatesCDF = parseInt(prompt("Quantos jogos o CDF FC empatou?"));
var pontosCDF = calculaPontos(vitoriasCDF, empatesCDF);
```

### 5. Comparação dos Pontos

Após calcular os pontos dos dois times, o código compara os resultados e exibe uma mensagem apropriada.

**Código:**
```javascript
if (pontosNJ > pontosCDF) {
  mostra("O time NJ está indo MELHOR que o CDF");
}
if (pontosNJ < pontosCDF) {
  mostra("O time NJ está indo PIOR que o CDF");
}
if (pontosNJ == pontosCDF) {
  mostra("O time NJ está EMPATADO com o CDF");
}
```

**Explicação:**  
- Se o número de pontos do NJ for maior que o do CDF FC, exibe que o NJ está indo melhor.
- Se for menor, exibe que o NJ está indo pior.
- Se for igual, indica que ambos estão empatados.
```
