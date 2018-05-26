# Arrays: Índice

O array por índice é o mais simples, vamos analisar o exemplo anterior:

```php
$nomes = ['Ada', 'Alefe', 'Charles'];

echo $nomes[0]; // Exibe: Ada
echo $nomes[2]; // Exibe: Charles
```

Nesse exemplo acessamos os valores utilizando o nome da variável seguido do índice entre colchetes a partir do zero, ou seja, _0_ retornará o primeiro valor, _1_ o segundo e assim por diante, no começo é difícil de aceitar isso mas com o tempo você se acostuma, pois é a mesma coisa na maioria (para não dizer todas) as linguagens de programação.

Os valores de um array em PHP podem ser de qualquer tipo, inclusive embora não seja recomendado, você pode misturar tipos:

```php
$nome = 'Alefe';
$array = [21, 'PHP', true, $nome];

echo $array[0]; // Exibe: 21
echo $array[1]; // Exibe: PHP
echo $array[3]; // Exibe: Alefe
```

Você também pode alterar o valor de itens no array da mesma forma que altera uma variável, exemplo:

```php
$nomes = ['Ada', 'Alefe', 'Charles'];

echo $nomes[0]; // Exibe: Ada

$nomes[0] = 'Lovelace';

// O valor da variável $nomes passa a ser: ['Lovelace', 'Alefe', 'Charles']

echo $nomes[0]; // Exibe: Lovelace
```
