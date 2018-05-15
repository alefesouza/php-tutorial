# Condicionais

Nas linguagens de programação é muito comum usarmos condicionais, que são blocos de código que serão executados se determinada condição for verdadeira, por exemplo:

```php
$var1 = 3;
$var2 = 2;

if ($var1 + $var2 == 5) {
    echo "$var1 + $var2 é igual a 5"; // Exibe na tela: 3 + 2 é igual a 5
} else {
    echo "$var1 + $var2 não é igual a 5 (?)";
}
```

Nesse caso a segunda condição nunca será executada, pois o valor da variável `$var1` somado com o valor da `$var2` é 5.

Detalhes como o `else` e condicionais mais avançadas serão abordadas na próxima página.
