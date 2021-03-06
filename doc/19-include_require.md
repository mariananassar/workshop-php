# Include

Conforme vamos avançando no desenvolvimento da nossa aplicação é possível que ela fique um tanto confusa com declarações de variáveis e functions em um único arquivo. No PHP você pode criar um arquivo separado contendo todas as variáveis, por exemplo, e depois incluí-lo no arquivo principal. Para isso, podemos utilizar a declaração `include` que inclui e avalia o arquivo informado. 

Veja o exemplo:

```php
vars.php // arquivo de variáveis

$fruta = 'maçã';
$cor = 'verde';


teste.php // arquivo de exemplo

include 'vars.php'; // pode usar também: include('vars.php');

echo "A $fruta é $cor "; // A maçã é verde
```
## Include_once
A declaração `include_once` inclui e avalia o arquivo informado durante a execução do script. Este é um comportamento similar a declaração include, com a única diferença que, como o nome sugere, **o arquivo será incluído somente uma vez**.

O `include_once` pode ser utilizado quando o mesmo arquivo é incluído mais de uma vez, neste caso, ajudará a evitar problemas como declaração de funções, classes ou constantes já existentes.

# Require

`require` é idêntico ao `include` exceto que em caso de falha produzirá um erro fatal, `E_COMPILE_ERROR`, ou seja, não compila. Enquanto que o `include` apenas emitirá um alerta `E_WARNING)` permitindo que o script continue. 


## Require_once

A declaração `require_once` é idêntica a `require` exceto que o PHP verificará se o arquivo já foi incluído, e em caso afirmativo, não o incluirá (exigirá) novamente.

# Diferença entre `include` e `require`?

Você já viu até aqui que as declarações de `include` e `require`são bem semelhantes. A única diferença é que `include`  gera apenas um aviso do PHP, mas permite que a execução do script continue se o arquivo a ser incluído não puder ser encontrado. Enquanto a `require` gerará um erro fatal e interromperá a execução do script.

[Voltar a página inicial](../README.md)