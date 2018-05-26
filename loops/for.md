# Comandos de repetição: for

Uma das principais características do ´for´ é ter meio que um contador embutido, vamos analisar o último exemplo:

```php
for ($i = 0; $i < 10; $i++) {
    echo $i . ' ';
}

// No final será exibido:
// 0 1 2 3 4 5 6 7 8 9
```

No exemplo acima o comando for possui três partes, separadas por ponto e vírgula dentro do parênteses, acontece o seguinte:

* Na primeira parte iniciamos uma variável chamada `$i` cujo valor inicial é **0**.
* Na segunda colocamos uma condicional, no caso queremos que o código dentro do for se repita enquanto o valor de `$i` seja menor que **10**.
* Na terceira parte dizemos o que irá acontecer quando o que estiver dentro do ´for´ for executado, no caso acrescentaremos **1** ao valor de `$i` a cada execução.

Desta maneira, a próxima vez que o bloco `for` for executado, o valor de `$i` será **1**, depois **2**, e assim por diante até `$i` ser igual a **10**, o que fará o código parar de repetir pois **10** não é menor que **10**, e sim igual, então o código após o `for` será executado normalmente.

Ele é muito útil caso você precise de um contador pois ele meio que te obriga a declarar um, podemos aproveitar o contador para fazer condicionais por exemplo:

```php
for ($i = 1; $i <= 5; $i++) {
    if ($i == 3) {
        echo 'Mensagem exibida se $i for igual a 3';
    }

    if ($i == 5) {
        echo 'Mensagem exibida se $i for igual a 5';
    }
}
```

Você também pode usá-lo para percorrer arrays usando a função global `count()`:

```php
$nomes = ['Alefe', 'Ada', 'Charles', 'Rasmus', 'Brendan'];

for ($i = 0; $i < count($nomes); $i++) {
    echo $nomes[$i] . ', ';
}

// No final será exibido:
// Alefe, Ada, Charles, Rasmus, Brendan,
```

Nesse caso o valor de `count($nomes)` será **6**, e então na primeira execução do for o valor de `$i` será **0**, assim exibindo o valor de `$nomes[0]`, depois `$nomes[1]`, e assim por diante até `$nomes[5]`.

Lembre-se que os arrays começam a partir do _0_, e o valor de `$i` só vai até _5_ (o índice máximo desse array) pois na segunda parte colocamos que será repetido enquanto `$i` for menor que `count($nomes)`.
