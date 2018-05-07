# Strings

Você também pode armazenar strings (textos) em variáveis e concatená-las (juntar) para formar uma nome string, para isso basta declarar a variável colocando entre aspas duplas ou aspas simples, como por exemplo:

```php
$nome = "Alefe";
$sobrenome = 'Souza';
$numero = 5;

echo $nome; // Alefe
echo $nome.$numero; // Alefe5
echo $nome . ' ' . $sobrenome; // Alefe Souza
```

Note que diferente da maioria das linguagem, no PHP se utiliza o . (ponto) para fazer a concatenação de strings, ao invés do +.

## A diferença de aspas simples e duplas:

```php
$aspasDuplas = "$nome $sobrenome";
$aspasSimples = '$nome $sobrenome';
$aspasSimplesConcatenando = $nome . ' ' . $sobrenome;

echo $aspasDuplas; // Alefe Souza
echo $aspasSimples; // $nome $sobrenome
echo $aspasSimplesConcatenando; // Alefe Souza
```

Quando você utiliza aspas duplas, você pode adicionar variáveis normalmente dentro do texto, no final essas variáveis serão substituídas pelo valor delas, isso não acontece quando declaramos com aspas simples, pode até parecer legal usar aspas duplas, porém o PHP precisa checar em toda declaração com aspas duplas se existe uma variável dentro, o que acaba perdendo um pouco em perfomance ("velocidade"), sendo recomendado sempre declarar strings com aspas simples.
