# Comandos de repetição: foreach

Com o foreach você pode percorrer arrays comuns e chave-valor de maneira fácil sem precisar de um contador, exemplo:

```php
$array = [1, 3, 5, 4, 6, 8];

foreach ($array as $item) {
    echo $item . ' ';
}

// No final exibe:
// 1 3 5 4 6 8
```

No exemplo acima, o comando de repetição `foreach` repete a mesma quantidade de itens do array, com a variável `$item` possuindo o valor do item referente aquela repetição, veja outro exemplo com strings:

```php
$nomes = ['Alefe', 'Ada', 'Charles'];

foreach ($nomes as $nome) {
    echo $nome . ', ';
}

// No final exibe:
// Alefe, Ada, Charles
```

Você também pode percorrer arrays chave-valor com o `foreach`, veja o exemplo a seguir:

```php
$dados = [
    'nome' => 'Alefe',
    'sobrenome' => 'Souza',
    'idade' => 21
];

foreach ($dados as $chave=>$valor) {
    echo $chave . ': ' . $valor . '<br>';
}

// No final exibe:
// nome: Alefe
// sobrenome: Souza
// idade: 21
```
