# Orientação a objetos

Caso você já tenha mexido com linguagens de programação como Java ou C#, deve saber o conceito de classes e orientação a objetos, no PHP é possível utilizar o mesmo conceito, analise o código em Java a seguir:

```java
public class Pessoa {
    private String primeroNome;
    private String ultimoNome;

    public Pessoa(String primeiroNomeParam, String ultimoNome) {
        this.primeroNome = primeiroNomeParam;
        this.ultimoNome = ultimoNome;
    }

    public String getNomeCompleto() {
        return this.primeroNome + ' ' + this.ultimoNome;
        // Também é possível:
        // return primeroNome + ' ' + ultimoNome;
    }
}

// Em outro arquivo
Pessoa pessoa1 = new Pessoa("Alefe", "Souza");
Pessoa pessoa2 = new Pessoa("James", "Gosling");

System.out.println(pessoa1.getNomeCompleto()); // Alefe Souza
System.out.println(pessoa2.getNomeCompleto()); // James Gosling
```

Agora a mesma classe, escrita em PHP:

```php
class Pessoa
{
    private $primeroNome;
    private $ultimoNome;

    public function __construct($primeroNomeArg, $ultimoNome)
    {
        // Associa o atributo $primeiroNome ao argumento $primeroNomeArg utilizando o $this.
        $this->primeiroNome = $primeiroNomeArg;
        // Também é possível que o atributo da classe e o argumento do método possuam o mesmo nome.
        $this->ultimoNome = $ultimoNome;
    }

    public function getNomeCompleto()
    {
        return $this->primeiroNome . ' ' . $this->ultimoNome;
    }
}

$pessoa1 = new Pessoa('Alefe', 'Souza');
$pessoa2 = new Pessoa('Rasmus', 'Lerdorf');

echo $pessoa1->getNomeCompleto(); // Alefe Souza
echo $pessoa2->getNomeCompleto(); // Rasmus Lerdorf
```

Não é o foco desse workshop entrar em detalhes sobre orientação a objetos, portanto fazendo uma comparação direta com as linguagens Java e C#:

* O método construtor não é um método com o mesmo nome da classe, e sim o método \_\_construct, que chamamos de "[método mágico](http://php.net/manual/pt_BR/language.oop5.magic.php)", que são métodos reservados das classes em PHP que fazem algo de especial.
* Para acessar métodos e atributos da própria classe, utizamos uma setinha: $variavel->atributo ao invés de variavel.atributo como nas outras linguagens.
* Note que não utilizamos o $ depois da ->, por mais confuso que isso possa parecer inicialmente.
* Obrigatoriamente temos que utilizar o $this-> para acessar métodos e atributos dentro da própria classe.
* Embora seja uma boa prática, não é obrigatório o nome da classe em PHP ter o mesmo nome do arquivo, também podemos escrever códigos normalmente antes e após a declaração da classe, mas reenforçando que isto não é uma boa prática.
