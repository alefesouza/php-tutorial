# Comandor de repetição: do...while

O comando de repetição `do...while` funciona da mesma forma do `while`, porém dessa vez a condição vem no final, garantindo que o código seja executado pelo menos uma vez, mesmo que a condição seja falsa inicialmente, exemplo:

```php
$i = 0;

do {
    echo $i . ' ';

    $i++;
} while ($i < 10);

// No final exibe:
// 0 1 2 3 4 5 6 7 8 9

$nome = 'Alefe';

do {
    echo $nome;
} while ($nome != 'Alefe');

// No final exibe: Alefe
```

No segundo exemplo, ele compara se pode repetir somente após a execução do código, por isso chega a exibir a mensagem.
