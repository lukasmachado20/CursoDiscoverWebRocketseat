# Box Model

* Fundamental para criação de layouts para Web.
* Dá maior facilidade para aplicar o CSS.

## O que é?

* Uma caixa retangular.
* Essa caixa possui propriedades de uma caixa 2D.

- Tamanho (largura x altura)             width | height
- Conteúdo                               content
- Bordas                                 border
- Preenchimento interno                  padding
- Espaço fora da caixa                   margin

*Cada elemento na sua página, será colocado em uma caixa*

## box-sizing

Como será calculado o tamanho total da caixa?

- Feito pelo content-box (o conteúdo da caixa)
* Ex: width: 100px vai somar com padding: 0 20px; -> totalizando 140px;

Como manter os verdadeiros 100px desejados?

```css
    div {
        box-sizing: border-box;
    }

    /* Para não atrapalhar a contagem das box no layout */
    * {
        box-sizing: border-box;
    }
```

## display: block vs display: inline

- Como as caixas se comportam em relação a outras
- Comportamento externo das caixas


| **block**                        | **inline**                     |
| Ocupa toda a linha, colocando    | Elemento ao lado do outro.     |
| o próximo elemento abaixo desse. |                                |
|----------------------------------|--------------------------------| 
| width e heigth são respeitados   | width e height não funcionam   |
|----------------------------------|--------------------------------|
| padding, margin, border irão     | Somente os valores horizontais |
| funcionar normalmente            | de margin, padding e border    |
|-------------------------------------------------------------------|


## Margin
* Margin, é o espaço (margem) entre os elementos

- Podemos dividir o margin em 4 valores:

- margin-top | margin-right | margin-bottom | margin-left 
- values: `<length>` | `<percentage>` | auto

- Geralmente usamos uma forma abreviada (shorthand) para escrever o margin. Esse formato segue o sentido horário iniciando pelo top, seguindo para right, bottom e left.

margin: 12px 16px 10px 4px; /* TOP = 12px | RIGHT = 16px | BOTTOM = 10px | LEFT = 4px */
margin: 12px 16px 0; /* TOP = 12px | RIGHT = 16px | BOTTOM = 0px | LEFT = 16px */
margin: 8px 16px; /* TOP = 8px | RIGHT = 16px | BOTTOM = 8px | LEFT = 16px */
margin: 8px; /* TOP = 8px | RIGHT = 8px | BOTTOM = 8px | LEFT = 8px */

O margin é aplicado em elementos com display block

*Cuidado com o margin collapsing que é quando o top se junta ao bottom*

## Padding

* O padding é o preenchimento interno da caixa.

* A propriedade padding pode ser escrita como nos formatos apresentados abaixo:

- padding-top | padding-right | padding-bottom | padding-left
* values: `<length>` | `<percentage>`

- Geralmente usamos uma forma abreviada (shorthand) para escrever o padding.
- Esse formato segue o sentido horário iniciando pelo top, seguindo para right, bottom e left.

- padding: 12px 16px 10px 4px; /* TOP = 12px | RIGHT = 16px | BOTTOM = 10px | LEFT = 4px
- padding: 12px 16px 0; /* TOP = 12px | RIGHT = 16px | BOTTOM = 0px | LEFT = 16px
- padding: 8px 16px; /* TOP = 8px | RIGHT = 16px | BOTTOM = 8px | LEFT = 16px 
padding: 8px; /* TOP = 8px | RIGHT = 8px | BOTTOM = 8px | LEFT = 8px */

- O padding pode ter valores (values) de comprimento (px, em, rem) ou de porcentagem (%)

*O padding poderá causar diferença na largura de um elemento*

* obs.: Na aula sobre box-xizing aprendemos como resolver essa diferença na largura do elemento
(https://app.rocketseat.com.br/node/uma-caixa-dentro-da-outra/lesson/box-sizing)

## Border

* São as bordas da caixa

* Documentação do MDN: https://developer.mozilla.org/en-US/docs/Web/CSS/border

- value: <border-style> | <border-width> | <border-color>

- style: solid | dotted | dashed | double | groove | ridge | inset | outset
- width: <length>
- color: <color>
```css
div {
	/* shorthand */
	border-top: solid 2px; /* top | right | bottom | left */

	/* style */
	border: solid;

	/* width <length> | style */
	border: 2px dotted;

	/* style | color */
	border: outset #f33;

	/* width | style | color */
	border: medium dashed green;

}
```

## E o outline?

- O outline é muito semelhante ao border, mas difere em 4 sentidos: Não modifica o tamanho da caixa, pois não é parte do Box Model.

- Poderá ser diferente de retangular.
- Não permite ajuste individuais.
- Mais usado pelo user agent para acessibilidade.