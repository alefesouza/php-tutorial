# Funções

Função é um modo de dar nome a um bloco de código e chamá-lo quantas vezes quiser, mudando o valor de apenas algumas coisas ou nenhuma, veja o exemplo a seguir:

```php
function soma($num1, $num2) {
    return $num1 + $num2;
}

echo soma(2, 3); // Exibe: 5
```

Analisando o código acima, usamos a palavra-chave `function` seguido do nome que queremos dar a função, e então colocamos entre parentes os argumentos da função, que funcionam como variáveis, podendo usar e ser modificado dentro do bloco da função.

Usamos a palavra-chave `return` para retorna algum valor ou parar a execução dela, o que não é obrigatório caso você queira apenas repetir um algoritmo, é comum ter um return vazio dentro de condicionais em funções que não retornam valor, exemplo:

```php
function teste($nome) {
    if ($nome == 'Alefe')  {
         echo 'Mensagem exibida se $nome for igual a Alefe';
         return;
    }

    echo 'A função continua se $nome não for igual a Alefe';
}

teste('Alefe'); // Exibe apenas o primeiro echo
teste('Rasmus'); // Exibe apenas o segundo echo
```

Caso não tivesse o `return` no exemplo acima, a chamada de função `teste('Alefe')` exibiria as duas mensagens.

Também não é obrigatório funções terem argumentos, você pode usá-las somente pra evitar repetição de código:

```php
function teste() {
  echo 'Mensagem 1<br>';
  echo 'Mensagem 2<br>';
  echo 'Mensagem 3<br>';
}

teste();
teste();
teste();
```

O código acima exibe 9 mensagens na tela, pois é chamada três vezes uma função que exibe três mensagens.

O corpo de uma função pode ter qualquer código PHP e os argumentos e retornos podem ser de qualquer tipo, números, strings, arrays e até outras funções.
