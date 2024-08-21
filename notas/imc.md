```markdown
# Documentação do Código: Calculadora de IMC

**Descrição:**

Este código é uma página HTML que calcula o Índice de Massa Corporal (IMC) de um usuário com base em seu peso e altura. O cálculo é feito utilizando JavaScript e o resultado é exibido na página. Além disso, a página fornece informações adicionais sobre a relação do IMC do usuário com os limites de magreza e obesidade severa.

## Estrutura do Código

### HTML Básico

```html
<!DOCTYPE html>
<html>
<head>
    <title>IMC</title>
</head>
<body>
  <!-- O código JavaScript será inserido aqui -->
</body>
</html>
```

- `<!DOCTYPE html>`: Declara o tipo de documento como HTML5.
- `<html>`: Elemento raiz do documento HTML.
- `<head>`: Contém metadados e o título da página.
- `<title>`: Define o título da página que aparece na aba do navegador.
- `<body>`: Contém o conteúdo visível da página. O código JavaScript é inserido dentro dessa seção.

### JavaScript

```javascript
<script>
  function pulaLinha() {
    document.write("<br>");
  }

  function mostra(frase) {
    document.write(frase);
    pulaLinha();
  }

  function calculaIMC(peso, altura) {
      var imc = peso / (altura * altura);
      return imc;
  }

  var nomeUsuario = prompt("Boa tarde! Qual é o seu nome?");
  var pesoDoUsuario = prompt("Bem vindo!(a) qual é o seu peso?");
  var alturaDoUsuario = prompt("E a sua altura?");
  var imcDoUsuario = calculaIMC(pesoDoUsuario, alturaDoUsuario);

  mostra(nomeUsuario + " seu imc é: " + imcDoUsuario.toFixed(2));
  mostra("Você ainda está " + (imcDoUsuario - 18.5).toFixed(2) + " pontos acima do limite da magreza");
  mostra("Você está " + (35 - imcDoUsuario).toFixed(2) + " longe da obesidade severa");
</script>
```

#### Função `pulaLinha`

```javascript
function pulaLinha() {
  document.write("<br>");
}
```
- Adiciona uma quebra de linha no documento HTML.

#### Função `mostra`

```javascript
function mostra(frase) {
  document.write(frase);
  pulaLinha();
}
```
- Recebe uma string (`frase`) e a escreve na página. Em seguida, chama a função `pulaLinha` para adicionar uma quebra de linha após o texto.

#### Função `calculaIMC`

```javascript
function calculaIMC(peso, altura) {
    var imc = peso / (altura * altura);
    return imc;
}
```
- Recebe o peso e a altura do usuário como parâmetros.
- Calcula o IMC usando a fórmula: `peso / (altura * altura)`.
- Retorna o valor calculado do IMC.

#### Interação com o Usuário

```javascript
var nomeUsuario = prompt("Boa tarde! Qual é o seu nome?");
var pesoDoUsuario = prompt("Bem vindo!(a) qual é o seu peso?");
var alturaDoUsuario = prompt("E a sua altura?");
```
- Usa a função `prompt` para obter o nome, peso e altura do usuário através de caixas de diálogo.

#### Cálculo e Exibição do IMC

```javascript
var imcDoUsuario = calculaIMC(pesoDoUsuario, alturaDoUsuario);

mostra(nomeUsuario + " seu imc é: " + imcDoUsuario.toFixed(2));
mostra("Você ainda está " + (imcDoUsuario - 18.5).toFixed(2) + " pontos acima do limite da magreza");
mostra("Você está " + (35 - imcDoUsuario).toFixed(2) + " longe da obesidade severa");
```
- Calcula o IMC do usuário chamando a função `calculaIMC`.
- Usa a função `mostra` para exibir o IMC do usuário e informações adicionais sobre sua condição em relação aos limites de magreza e obesidade severa.

**Explicações Adicionais:**

- `document.write` é usado para escrever diretamente no documento HTML. Embora seja útil para testes, geralmente não é recomendado para aplicações reais devido a problemas com a substituição do conteúdo da página e falta de flexibilidade. Para projetos mais avançados, considere usar métodos modernos como `innerHTML` ou manipulação do DOM com JavaScript.

- `.toFixed(2)` é utilizado para formatar o número do IMC com duas casas decimais.
```
