# Résumé

## getElementById()

O método `getElementById()`, como o próprio nome explicita, recolhe um elemento no corpo do html, pelo seu atributo `id`.

HTML:

``` html
<div id="time-peq">Vasxcão</div>
<div id="time-gig">Ibis</div>
```

JS:

``` js
console.log(
    document.getElementById('time-gig')
)
```

No trecho JS acima, além de recolher o elemento, o método `console.log()` retorna o valor no console do navegador, assim que o script é carregado.

## getElementsByClassName()

Este método recolhe elementos pelo atributo `class`, a diferença para o método `getElementById()`, é que normalmente definimos um nome de `class` para elementos distintos. Assim, este método constrói um array de elementos que pertenceriam a esta classe, mesmo que no corpo html só haja um elemento com esta classe atribuída, neste caso, criando um array de tamanho 1.

```html
<script>
        /* getELementById()
        console.log(
            document.getElementById("time-gig"),
            document.getElementById("time-gig").innerHTML
        );
        */

        // getElementsByClassName()
        var fala_ = document.getElementsByClassName('shrek').innerHTML;
        var fala_shrek = document.getElementsByClassName('shrek')[0].innerHTML;
        var fala_burro = document.getElementsByClassName('burro')[0].innerHTML;
        var dialog = ["- " + fala_, "- " + fala_shrek, "- " + fala_burro];

        for(i=0; i<dialog.length; i++){
            console.log(dialog[i]);
        }
    </script>
```

A variável `fala_`, posta desta forma, é o dito array de elementos da classe. Enquanto `fala_shrek` e `fala_burro` utilizam `[0]`, ou seja, selecionam o primeiro elemento do array, que no caso é o primeiro elemento com a classe. Analise o console para verificar a saída.

## getElementsByTagName()

Conceito semelhante ao do método `getElementsByClassName()`, em relação a formação de array de elementos. 

```js
    console.log(
        document.getElementsByTagName('button'),
        document.getElementsByTagName('button')[0],
        document.getElementsByTagName('button')[0].innerHTML
    );
```

No trecho, o primeiro argumento de `console.log()` retorna o array de tamanho 1. O segundo argumento retorna o primeiro elemento deste array. E o terceiro argumento retorna o conteúdo deste primeiro elemento.