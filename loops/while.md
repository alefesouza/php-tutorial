# While

No comando de repetição while, o código será repetido mediante determinada condição, da mesma forma que você usa no `if`:

```php
$i = 0;

while ($i < 10) {
    echo $i . ' ';

    $i++;
}

// No final exibe:
// 0 1 2 3 4 5 6 7 8 9
```

No exemplo acima, o código dentro do `while` será repetido `enquanto` (tradução de while) a condição for verdadeira, ou seja, ela irá parar assim que `$i` for igual a **10**, pois a condição diz que quer que `$i` seja menor que **10**.

Eu fiz um contador por ser a melhor forma de explicar, mas diferente do `for` você não precisa necessariamente declarar um, poderia ser qualquer condição ali no `while`, que ela seria repetida até a mesma ser falsa.
