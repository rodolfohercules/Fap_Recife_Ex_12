# Instruções:

Faça, utilizando o Google Blockly, uma função calculadora que os números e as operações serão feitas pelo usuário. O código deve ficar rodando infinitamente até que o usuário escolha a opção de sair. No início, o programa mostrará a seguinte lista de operações:

- 1: Soma
- 2: Subtração
- 3: Multiplicação
- 4: Divisão
- 0: Sair

Digite o número para a operação correspondente e caso o usuário introduza qualquer outro, o sistema deve mostrar a mensagem “Essa opção não existe” e voltar ao menu de opções.

Após a seleção, o sistema deve pedir para o usuário inserir o primeiro e segundo valor, um de cada. Depois precisa executar a operação e mostrar o resultado na tela. Quando o usuário escolher a opção “Sair”, o sistema irá parar.

É necessário que o sistema mostre as opções sempre que finalizar uma operação e mostrar o resultado.

# Resolução:

<img src='x.png'>

- Link para acessar: https://blockly-demo.appspot.com/static/demos/code/index.html?lang=pt-br

# Código

```
var opcao, numero1, numero2;


while (true) {
  window.alert('Escolha uma das opções: ');
  window.alert('1: SOMA');
  window.alert('2: SUBTRAÇAO');
  window.alert('3: MULTIPLICAÇAO');
  window.alert('4: DIVISAO');
  window.alert('0: SAIR');
  opcao = Number(window.prompt('insira a opção desejada:'));
  if (opcao < 0 || opcao > 4) {
    window.alert('Esta opção não existe.');
  } else {
    if (opcao == 0) {
      break;
    }
    numero1 = Number(window.prompt('insira qual o primeiro número:'));
    numero2 = Number(window.prompt('insira qual o segundo número:'));
    if (opcao == 1) {
      window.alert('A soma dos números é:' + String(numero1 + numero2));
    } else if (opcao == 2) {
      window.alert('A subtração dos números é:' + String(numero1 - numero2));
    } else if (opcao == 3) {
      window.alert('A multiplicação dos números é:' + String(numero1 * numero2));
    } else if (opcao == 4) {
      window.alert('A divisão dos números é: ' + String(numero1 / numero2));
    }
  }
}
```