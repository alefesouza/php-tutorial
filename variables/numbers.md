# Variáveis: Números

Você também pode armazenar números e operações matemáticas em variáveis, e até fazer operações matemáticas com duas variáveis, por exemplo:

```php
$var1 = 1.5;
$var2 = 3 + 2;
$var3 = $var2 - $var1;
$var4 = 4 * $var2;
$var5 = 5 / 2;

echo $var1; // Exibe: 1.5
echo $var2; // Exibe: 5
echo $var3; // Exibe: 3.5, resultado de 5 - 1.5
echo $var4; // Exibe: 20, resultado de 4 vezes 5
echo $var5; // Exibe: 2.5
```

{% exercise %}
Crie uma variável chamada `$calculo` com qualquer operação matemática cujo resultado seja `10`.
{% solution %}
$calculo = 5 + 5;
{% validation %}
assert($calculo == 10);
{% endexercise %}
