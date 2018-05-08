# Condicionais: switch

Com o comando switch podemos realizar diversas comparações ao mesmo tempo, não precisando declarar vários else if, como no exemplo a seguir:

```php
$numero = 5;

switch ($numero) {
    case 1:
        echo 'O valor de $numero é 1';
        break;
    case 3:
    case 4:
        echo 'O valor de $numero é 3 ou 4';
        break;
    case 5:
        echo 'O valor de $numero é 5'; // Será exibido na tela
        break;
    default:
        echo 'O valor de $numero não corresponde aos condicionais anteriores';
        break;
}
```

Veja o mesmo código utilizando o if:

```php
$numero = 5;

if ($numero == 1) {
    echo 'O valor de $numero é 1';
} else if ($numero == 3 || $numero == 4) {
    echo 'O valor de $numero é 3 ou 4';
} else if ($numero == 5) {
    echo 'O valor de $numero é 5'; // Será exibido na tela
} else {
    echo 'O valor de $numero não corresponde aos condicionais anteriores';
}
```

Ele é muito útil para deixar o código mais limpo e escrever menos códigos caso tenha ainda mais condicionais, você também pode usá-lo com strings:

```php
$nome = 'Alefe';

switch ($nome) {
    case 'Rasmus':
        echo 'O valor de $nome é Rasmus';
        break;
    case 'Alefe':
        echo 'O valor de $nome é Alefe'; // Será exibido na tela
        break;
    case 'Brendan':
    case 'Dennis'
        echo 'O valor de $nome é Brendan ou Dennis';
        break;
    default:
        echo 'O valor de $nome não corresponde aos condicionais anteriores';
        break;
}
```
