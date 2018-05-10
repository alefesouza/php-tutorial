# Funções globais

O PHP possui **muitas** funções globais úteis para o dia a dia do desenvolvedor, elas estão sempre disponíveis sem você precisar importar nada, vou citar algumas das mais simples e utilizadas:

## Retornar números de itens em um array

```php
$array1 = [5, 9, 7, 5, 3, 8, 9];
$array2 = ['Alefe', 'Rasmus', 'Brandan'];

echo count($array1); // Exibe: 7
echo count($array2); // Exibe: 3
```

Você pode usar o valor retornado normalmente como um número comum, pois é um número.

## Verificar se determinada string possui outra

```php
$frase = 'PHP é um linguagem de programação';

if (strpos($frase, 'linguagem') !== false) {
    echo 'A variável $frase possui a palavra "linguagem"';
}
```

É meio estranho essa comparação !== false, mas tem toda uma história por causa do PHP ser uma linguagem fracamente tipada e ter se originado do C, seria tão bom se fosse simplesmente "string".contains("")...

## Mudar uma parte de uma string por outra

```php
$frase = 'PHP é um linguagem de programação';

echo str_replace('PHP', 'JavaScript', $frase); // Exibe: JavaScript é uma linguagem de programação
```

## Ordernar um array

```php
$array = [5, 9, 7, 3, 8];

sort($array);

// Valor de $array passa a ser:
// [3, 5, 7, 8, 9]
```

Você pode ver funções globais na documentação oficial do PHP, aqui estão alguns exemplos em português de funções globais para [variáveis](http://php.net/manual/pt_BR/book.var.php), [strings](http://php.net/manual/pt_BR/book.strings.php) e [arrays](http://php.net/manual/pt_BR/book.array.php).
