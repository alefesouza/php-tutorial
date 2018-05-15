# Arrays

Explicando de forma muito simples, arrays são formas de armazenar vários valores em uma só variável, muito útil quando precisamos armazenar listas ou algo que seja múltipla coisa, veja o exemplo de array a seguir:

```php
$nomes = ['Ada', 'Alefe', 'Charles'];

echo $nomes[0]; // Exibe: Ada
echo $nomes[2]; // Exibe: Charles
```

Note que armazenamos três valores na variável nome, e podemos acessá-los utilizando o nome da variável seguido do número do índice ou chave entre colchetes.

Pode ser que você encontre arrays sendo declarados da seguinte forma:

```php
$nomes = array('Ada', 'Alefe', 'Charles');
```

Em versões muito antigas do PHP essa era a única forma de declarar arrays, mas só muda usar `array(valores)` ao invés de `[valores]`, o resto funciona da mesma forma.
