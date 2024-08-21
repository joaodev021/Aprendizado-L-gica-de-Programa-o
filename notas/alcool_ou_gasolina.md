# Análise do Exercício "Álcool ou Gasolina?"

## Descrição do Exercício
Este exercício tem como objetivo determinar qual combustível é mais vantajoso entre álcool e gasolina, calculando o custo por quilômetro rodado com cada um.

## Análise Detalhada do Código

### 1. Estrutura HTML Básica
``
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Álcool ou Gasolina?</title>
  </head>
  <body>
    <h3>Álcool ou Gasolina?</h3>
    <!-- O script JavaScript será inserido aqui -->
  </body>
</html>
```
- <!DOCTYPE html>: Declara o tipo de documento, informando ao navegador que este é um documento HTML5.
- <html>: Contém todo o conteúdo da página web.
- <head>: Inclui metadados, como o charset e o título da página. O charset define a codificação de caracteres (UTF-8).
- <body>: Contém o conteúdo visível da página, incluindo o cabeçalho `<h3>` e o script JavaScript.

### 2. Função `pulaLinha`
```javascript
function pulaLinha() {
    document.write("<hr>");
}
```
- Função `pulaLinha()`: Esta função é responsável por adicionar uma linha horizontal (`<hr>`) no documento HTML. Ela serve para separar visualmente diferentes seções de texto geradas pelo script.

### 3. Variáveis e Cálculos para Gasolina
```javascript
var caminhoComGasolina = 480;
var consumoComGasolina = 40;
var mediaGasolina = caminhoComGasolina / consumoComGasolina;
var precoGasolina = 2.90;
var precoPorKmGasolina = precoGasolina / mediaGasolina;
```
- caminhoComGasolina: Representa a distância percorrida com gasolina (480 km).
- consumoComGasolina: Representa a quantidade de combustível consumido (40 litros).
- mediaGasolina: Calcula o consumo médio, ou seja, quantos quilômetros o carro percorre por litro de gasolina (480 km / 40 litros = 12 km/l).
- precoGasolina: Preço por litro da gasolina (R$ 2,90).
- precoPorKmGasolina: Calcula o custo por quilômetro rodado com gasolina, dividindo o preço do litro pela média de consumo (R$ 2,90 / 12 km/l = R$ 0,2417 por km).

### 4. Variáveis e Cálculos para Álcool
```javascript
var caminhoComAlcool = 300;
var consumoComAlcool = 40;
var mediaAlcool = caminhoComAlcool / consumoComAlcool;
var precoAlcool = 2.40;
var precoPorKmAlcool = precoAlcool / mediaAlcool;
```
- caminhoComAlcool: Representa a distância percorrida com álcool (300 km).
- consumoComAlcool: Representa a quantidade de combustível consumido (40 litros).
- mediaAlcool: Calcula o consumo médio, ou seja, quantos quilômetros o carro percorre por litro de álcool (300 km / 40 litros = 7,5 km/l).
- precoAlcool: Preço por litro do álcool (R$ 2,40).
- precoPorKmAlcool: Calcula o custo por quilômetro rodado com álcool, dividindo o preço do litro pela média de consumo (R$ 2,40 / 7,5 km/l = R$ 0,32 por km).

### 5. Saída dos Resultados
```javascript
document.write("Consumo com gasolina é: " + mediaGasolina.toFixed(2));
pulaLinha();
document.write("O preço por Km da gasolina é: " + precoPorKmGasolina.toFixed(2));
pulaLinha();
document.write("Consumo com Alcool é: " + mediaAlcool.toFixed(2));
pulaLinha();
document.write("O preço por Km do alcool é: " + precoPorKmAlcool.toFixed(2));
pulaLinha();
```
- document.write(): Insere texto ou HTML no documento. Neste caso, ele exibe o consumo médio e o preço por quilômetro tanto para gasolina quanto para álcool.
- toFixed(2): Formata o número com duas casas decimais para melhorar a legibilidade dos resultados.

### 6. Comparação e Decisão
```javascript
if (precoPorKmGasolina < precoPorKmAlcool) {
    document.write("<br>Gasolina é mais vantajosa.");
} else {
    document.write("<br>Álcool é mais vantajoso.");
}
```
- Condicional `if-else: Compara o custo por quilômetro entre gasolina e álcool.
  - Se o custo por quilômetro da gasolina (`precoPorKmGasolina`) for menor que o do álcool (`precoPorKmAlcool`), a gasolina é considerada mais vantajosa, e uma mensagem correspondente é exibida.
  - Caso contrário, o álcool é considerado mais vantajoso.

### Resumo
Esse script realiza uma comparação simples entre os custos de dirigir com gasolina e álcool. Ele calcula o consumo médio e o custo por quilômetro de cada combustível e exibe o resultado ao usuário, ajudando a determinar qual combustível é mais econômico para o motorista.
