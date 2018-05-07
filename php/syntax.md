# Sintaxe

A sintaxe do PHP inicialmente lembra bastante a do JavaScript, dificilmente usamos tipagem
e declaramos funções, segue o hello world (script mais básico) do PHP:

```php
// Arquivo: index.php
<?php

echo 'Hello World';

?>
```

Esse código gera o seguinte:

![Saída do Hello World](./assets/syntax/hello-world.png)

Analisando o código acima, iniciamos com um comentário apenas para indicar que estamos editando um arquivo chamado "index.php", como você pode ver o index.php na barra de endereços da imagem acima.

Apenas o que estiver dentro de `<?php ?>` será processado pelo PHP, o que estiver fora disso, será enviado normalmente para o navegador como HTML, caso você vá escrever apenas código PHP em um arquivo, é recomendado você não colocar o fechamento `?>`.

Tudo que estiver após o `echo` será enviado para o navegador, pode ser um texto (string), operações matemáticas, variáveis, etc.

Todo comando como declaração de variáveis, chamada de funções e o echo, deve terminar como ; (ponto e vírgula), se não terá uma mensagem de erro de sintaxe.
