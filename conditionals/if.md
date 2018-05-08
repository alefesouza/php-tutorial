# Condicionais: if

Com o comando if (se) podemos fazer comparações, executando um código se determinada condição for verdadeira e, caso queira, adicionar mais condições que podem executar outros códigos caso a primeira condição não for verdadeira, e por fim executar outro código caso não passe em nenhuma das condições anteriores, observe os exemplos a seguir:

```php
$nome = 'Alefe';

if ($nome == 'Alefe') {
    echo 'O valor da variável $nome é Alefe';
} else {
    echo 'O valor da variável $nome não é Alefe';
}
```

Note que usamos o comparador == para verificar o valor da variável $nome, que se caso for igual a 'Alefe', executará o primeiro bloco de código, senão (else) executará o segundo.

Podemos também fazer comparações com números:

```php
$numero = 5;

if ($numero > 10) {
    echo 'A variável $numero é maior que 10';
} else if ($numero > 7) {
    echo 'A variável $numero é maior que 7';
} else if ($numero >= 5) {
    echo 'A variável $numero é maior ou igual a 5'; // esse código será executado
} else if ($numero >= 3) {
    echo 'A variável $numero é maior ou igual a três';
} else {
    echo 'A variável $numero possui um valor diferente das condicionais anteriores';
}
```

Note que apenas a terceira condição será executada, pois ela possui um valor maior ou igual a 5 e é a primeira a ser verdadeira, pois não passa em nenhuma das condições anteriores, porém as condições seguintes, como a que compara se a variável $numero é maior ou igual a 3, não serão executadas por estarem no mesmo else if, apenas uma condição pode ser executada em um if com várias condições, mas você pode iniciar novas condicionais normalmente, bastando apenas não colocar "else" antes do comando "if", no próximo código há um exemplo.

Existem outras condicionais, para comparar se um número é menor que outro ou se determinado valor é diferente, por exemplo:

```php
$numero = -5;

if ($numero > 0) {
    echo 'A variável $numero é um número positivo';
} else if ($numero < 0) {
    echo 'A variável $numero é um número negativo'; // Será exibido na tela
} else if ($numero == 0) {
    echo 'A variável $numero é igual a 0';
} else {
    echo 'A variável $numero não é um número';
}

if ($numero != 5) {
    echo 'A variável $numero é diferente de 5'; // Será exibido na tela
} else {
    echo 'A variável $numero é igual a 5;
}
```

## Múltiplas condições

Assim como outras linguagens de programação podemos realizar múltiplas condições, no código a seguir, todos os blocos serão executados:

```php
$numero = 5;
$nome = 'Alefe';

if ($numero >= 3 && $numero <= 7) {
    echo 'A variável $numero é maior ou igual a 3 e menor ou igual a 7';
}

if ($numero == 5 || $numero == 3) {
    echo 'A variável $numero é igual a 5 ou igual a 3';
}

if ($numero != 7 && $nome == 'Alefe') {
    echo 'A variável $numero é diferente de 7 e a variável $nome é igual a "Alefe"';
}
```
