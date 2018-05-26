# Arrays: Multidimensional

Os arrays multidimensionais são arrays que possuem outros arrays dentro, exemplo:

```php
$array = [[5, 3, 7], [2, 9, 6]];

echo $array[0][2]; // Exibe: 7
echo $array[1][0]; // Exibe: 2
```

No exemplo acima, o primeiro `echo` exibe **7** pois no primeiro array (índice _0_) ele está pegando o terceiro item (índice _2_, contando a partir do 0), já o segundo `echo` exibe **2** pois segundo array (índice _1_) está pegando o primeiro item (índice _0_).

Podemos fazer a mesma coisa com o array chave-valor, exemplo:

```php
$array = [
    [
        'nome' => 'Alefe',
        'sobrenome' => 'Souza'
    ],
    [
        'nome' => 'Rasmus',
        'sobrenome' => 'Lerdorf'
    ]
];

echo $array[0]['nome']; // Exibe: Alefe
echo $array[1]['sobrenome']; // Exibe: Lerdorf
```

No exemplo acima, o primeiro `echo` exibe **Alefe** pois no primeiro array (índice _0_) ele está pegando a chave _nome_, já o segundo `echo` exibe **Lerdorf** pois segundo array (índice _1_) está pegando a chave _sobrenome_.

Você pode incluir ainda mais arrays dentro de arrays, para acessar o valor você só precisa adicionar mais colchetes, exemplo:

```php
$array = [
    [
        [4, 6, 0],
        [3, 7, 2]
    ],
     // Índice 1
    [
        // Índice 0
        [2, 8, 5], // O índice 2 é 5
        [1, 9, 3]
    ]
];

echo $array[1][0][2]; // Exibe 5
```

E assim por diante.
