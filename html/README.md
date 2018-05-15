# Uso com HTML

Uma das melhores coisas do PHP (ou piores, se usada de maneira errada) é poder ser usado em conjunto com código HTML, de forma que você pode colocar condicionais que exibem um código HTML ou outro, usar loops para exibir listas, etc.

Lembra do começo do HTML onde falado que devemos usar o `?>` apenas quando não tiver apenas HTML no arquivo? Veja o exemplo a seguir:

```html
<b><?php echo 2 + 3; ?></b>
```

Quando executarmos o arquivo com esse código no navegador, ele exibirá:

**5**

Isso ocorre porque apenas o código dentro de `<?php ?>` será processado pelo PHP, o que estiver fora dele será enviado como HTML normalmente para o navegador, como as tags `<b>`, que deixam o texto em negrito, junto com o resultado final dos `echo` que colocamos, exatamente onde colocamos, ou seja, o que o navegador receberá será:

```html
<b>5</b>
```

Podemos também fazer condicionais e enviar determinado HTML para o navegador dependendo delas:

```html
<?php
$nome = 'Alefe';

if ($nome == 'Alefe') { ?>
<i>O valor de $nome é <?= $nome; ?></i>
<?php } else { ?>
<i>O valor de $nome não é Alefe, seu valor é <?= $nome; ?></i>
} ?>
```

Quando executarmos um arquivo com esse código no navegador, ele exibirá:

_O valor de $nome é Alefe_

Note que abrimos e fechamos várias vezes o `<?php ?>` para dizer que é uma continuação, há também a shorttag `<?= $variavel; ?>`, que é apenas uma simplificação de `<?php echo $variavel; ?>`, ou seja, serve apenas para exibir algum valor na tela.

Caso o valor de `$nome` fosse outro, como por exemplo Rasmus, exibiria na tela:

_O valor de $nome não é Alefe, seu valor é Rasmus_

Podemos fazer o mesmo com loops por exemplo, veja o exemplo a seguir:

```html
<?php
$nomes = ['Alefe', 'Ada', 'Charles'];
?>
<ul>
<?php foreach($nomes as $nome) { ?>
    <li><?= $nome; ?></li>
<?php } ?>
</ul>
```

O código enviado HTML para o navegador será:

```html
<ul>
    <li>Alefe</li>
    <li>Ada</li>
    <li>Charles</li>
</ul>
```

Que exibirá um lista igual a seguir:

* Alefe
* Ada
* Charles

Embora pareça muito legal, não é uma boa prática deixar lógica e HTML no mesmo arquivo, pois conforme o projeto cresce, pode deixar o código feio e confuso, houve uma época que isso era muito comum e acabou deixando o PHP com uma certa má fama por ser comum misturar todo o código em um único arquivo.

Assim como em qualquer outra linguagem de back-end, o ideal seria utilizar algum framework para gerenciar melhor o código PHP (controller) e o HTML (view), mas como o foco desse tutorial é apenas dar uma introdução, no momento o melhor que podemos fazer seria deixar todo o código PHP em um arquivo e o código HTML em outro, apenas exibindo o valor das variáveis, caso você tenha mais interesse na linguagem, recomendo estudar algum framework PHP, existem vários, os mais famosos são [Zend](https://framework.zend.com), [Symfony](https://symfony.com), [CodeIgniter](https://codeigniter.com), [CakePHP](https://cakephp.org), e o meu favorito, [Laravel](http://laravel.com).

Continuando o tutorial, existe a função global `include`, no qual você adicionar todo o código de um arquivo PHP em outro, veremos um separação e lógica e HTML no exemplo a seguir:

```php
// arquivo index.php
<?php

$dados = [
    'nome' => 'Alefe',
    'sobrenome' => 'Souza',
    'idade' => 21
];

include('views/index.php');
```

Agora o código do arquivo index.php dentro da pasta views:

```html
<!-- views/index.php -->
<p><b>Nome:</b> <?= $dados['nome']; ?></p>
<p><b>Sobrenome:</b> <?= $dados['sobrenome']; ?></p>
<p><b>Idade:</b> <?= $dados['idade']; ?> anos</p>
```

O código enviado HTML para o navegador será:

```html
<p><b>Nome:</b> Alefe</p>
<p><b>Sobrenome:</b> Souza</p>
<p><b>Idade:</b> 21 anos</p>
```

Que exibirá o seguinte no navegador:

**Nome:** Alefe

**Sobrenome:** Souza

**Idade:** 21 anos
