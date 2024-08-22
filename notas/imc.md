# Cálculo do IMC - Documentação

## Descrição

Este código é um programa simples em JavaScript que calcula o Índice de Massa Corporal (IMC) de um usuário. O IMC é uma medida utilizada para avaliar se uma pessoa está dentro do peso ideal com base em sua altura e peso. O programa solicita ao usuário seu nome, peso e altura, calcula o IMC, e exibe uma mensagem personalizada com o resultado e uma interpretação do IMC.

## Estrutura do Código

### HTML Básico

```html
<!DOCTYPE html>
<html>
<head>
    <title>IMC</title>
</head>
<body>
  <!-- O código JavaScript é inserido aqui -->
</body>
</html>
```

O código HTML serve como estrutura para a página web. Neste caso, ele contém a tag `head` onde está o título da página (`IMC`), e a tag `body`, onde o código JavaScript é executado.

### Funções JavaScript

#### `pulaLinha()`
```javascript
function pulaLinha() {
  document.write("<br>");
}
```
- Objetivo: Essa função insere uma quebra de linha (`<br>`) na página, permitindo que o conteúdo seja exibido em linhas separadas.
- Uso: Facilitar a formatação do texto exibido.

#### `mostra(frase)`
```javascript
function mostra(frase) {
  document.write(frase);
  pulaLinha();
}
```
- Objetivo: Exibir uma frase no documento HTML e adicionar uma quebra de linha logo em seguida.
- Uso: Para mostrar mensagens e resultados ao usuário.

#### `calculaIMC(peso, altura)`
```javascript
function calculaIMC(peso, altura) {
  return peso / (altura * altura);
}
```
- Objetivo: Calcular o IMC do usuário utilizando a fórmula:
  \[
\text{IMC} = \frac{\text{peso}}{\text{altura}^2}
\]
- Parâmetros:
  - `peso`: Peso do usuário em quilogramas.
  - `altura`: Altura do usuário em metros.
- **Retorno**: O valor do IMC.

### Interação com o Usuário

```javascript
var nomeUsuario = prompt("Boa tarde! Qual é o seu nome?");
var pesoDoUsuario = prompt("Bem vindo!(a) qual é o seu peso?");
var alturaDoUsuario = prompt("E a sua altura?");
```

- Objetivo: Coletar informações do usuário.
- Função `prompt()`: Exibe uma caixa de diálogo para o usuário inserir dados.
- Variáveis:
  - `nomeUsuario`: Armazena o nome do usuário.
  - `pesoDoUsuario`: Armazena o peso do usuário.
  - `alturaDoUsuario`: Armazena a altura do usuário.

### Cálculo e Exibição do IMC

```javascript
var imcDoUsuario = calculaIMC(pesoDoUsuario, alturaDoUsuario);
mostra(nomeUsuario + " seu imc é: " + imcDoUsuario.toFixed(2));
```

- Cálculo do IMC: Chama a função `calculaIMC()` passando o peso e a altura do usuário, armazenando o resultado na variável `imcDoUsuario`.
- Exibição do IMC: A função `mostra()` exibe o IMC do usuário, formatado com duas casas decimais usando `toFixed(2)`.

### Interpretação do IMC

```javascript
if(imcDoUsuario < 18.5) {
  mostra("Seu IMC indica você está ABAIXO do peso");
}

if(imcDoUsuario > 35) {
  mostra("Seu IMC indica que você está ACIMA do peso");
}

if(imcDoUsuario >= 18.5 && imcDoUsuario <= 35) {
  mostra("OK! Seu IMC está entre os dois limites");
}
```

- Condições:
  - Abaixo do peso: Se o IMC for menor que 18,5.
  - Acima do peso: Se o IMC for maior que 35.
  - Peso saudável: Se o IMC estiver entre 18,5 e 35, inclusive.
- Mensagens: Dependendo do valor do IMC, uma mensagem específica é exibida para o usuário.

## Considerações Finais

Este código é uma excelente introdução ao uso de JavaScript para manipulação de dados e interação com o usuário. Através dele, você praticou a criação de funções, o uso de condições (`if`) e a exibição de resultados em uma página HTML.
