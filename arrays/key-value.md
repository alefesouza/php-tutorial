# Arrays: Chave-Valor

Com o array chave-valor você pode usar palavras-chave ao invés de índices para armazenas valores em um array, exemplo:

```php
$array = [
    'nome' => 'Alefe',
    'sobrenome' => 'Souza'
];

echo $array['nome']; // Exibe: Alefe
echo $array['sobrenome']; // Exibe: Souza

// Podemos alterar o valor de uma chave da mesma forma
$array['sobrenome'] = 'Pereira';

// O array passa a ser ['nome' => 'Alefe', 'sobrenome' => 'Pereira']
echo $array['sobrenome']; // Exibe: Pereira
```

Como vimos no exemplo acima, podemos atribuir uma chave a um valor na declaração de um array utilizando `=>`, porém para alterar o valor após a declaração usamos o `=` (igual), também deve ser alterado um de cada vez.
