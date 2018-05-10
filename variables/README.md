# Variáveis

Variáveis são muito comuns na programação, são formas de guardar determinado valor em uma "palavra" para utilizar depois, no PHP elas não possuem tipagem, ou seja, você não precisa declarar que elas vão receber textos ou números por exemplo.

Para declar uma várivel em PHP, você precisa utilizar o símbolo $ seguido do nome da variável, exemplo:

```php
$nome = "Alefe";
$idade = 21;

echo $nome; // Exibe na tela: Alefe
echo $idade; // Exibe na tela: 21
```

{% exercise %}
Crie uma variável chamada `linguagem` com valor `php`.
{% solution %}
$linguagem = 'php';
{% validation %}
assert($linguagem == 'php');
{% endexercise %}