# Comandos de repetição: continue e break

Com as palavras-chaves `continue` e `break` podemos pular ou parar a execução de qualquer um dos comandos de repetição mencionados anteriormente, veja o exemplo a seguir:

```php
for ($i = 0; $i < 10; $i++) {
    if ($i == 4 || $i == 6) {
        continue;
    }

    if ($i == 8) {
        break;
    }

    echo $i;
}

echo 'Final';

// No final será exibido:
// 0 1 2 3 5 7 Final
```

O que aconteceu no exemplo acima é que quando o valor de `$i` for igual a **4** ou **6**, o `for` irá para a próxima execução ignorando tudo depois do `continue`, como o `echo` o final do mesmo, já quando o valor de `$i` for igual a **8** a repetição irá parar e continuar o código fora dela, assim ignorando a repetição cujo valor de `$i` seria **9** e o restante do código.

Você também pode usar essas palavras-chaves nos comandos `while`, `do...while` e `foreach`.
