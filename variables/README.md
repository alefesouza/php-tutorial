# Variáveis

Variáveis são muito comuns na programação, são formas de guardar determinado valor em uma "palavra" para utilizar depois, no PHP elas não possuem tipagem, ou seja, você não precisa declarar que determinada variável irá receber apenas textos ou números por exemplo.

Para declarar uma variável em PHP, você precisa utilizar o símbolo $ seguido do nome da variável, exemplo:

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
