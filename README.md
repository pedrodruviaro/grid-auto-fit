# Grid **_auto-fit_**

## Criando layouts com CSS Grid de forma fácil

---

### <code>**grid-template-columns: repeat(auto-fit, minmax(min, max))**</code>

-   _repeat_: enquanto houver a possibilidade de criar colunas, faça.
-   _auto-fit_: encaixe os elementos na coluna, com tamanho variável. Mas qual tamanho?
-   _minmax()_: função que define o tamanho das colunas. O primeiro argumento da função é o tamanho MÍNIMO da coluna, e o segundo, o tamanho MÁXIMO. Exemplo: <code>minmax(200px, 500px)</code>. A coluna terá um tamanho mínimo de 200 pixels e um máximo de 500 píxels. Enquanto houver a possibilidade de enxaicar as colunas tomando como base 200 píxels, o grid irá fazer.

-   No exemplo do código: <code>**grid-template-columns: repeat(auto-fit, minmax(18rem, 1fr));**</code>
    -   utilizando <code>**1fr**</code> como tamanho máximo: auxilia na responsividade. Se definirmos um tamanho mínimo coerente, 1fr definirá apenas <code>**uma**</code> coluna em dispositivos mobile.
    -   <code>**18rem**</code> como tamanho mímimo: se o grid conseguir encaixar duas colunas com <code>**18rem**</code> de tamanho MAIS o gap definido, uma coluna é adicionada. Enquanto a adição não ocorre, a coluna em questão é esticada, pois o tamanho máximo definido é variável também.

**Referências:**

CSS Grid
https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout

Grid Template Columns
https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template-columns

Minmax()
https://developer.mozilla.org/en-US/docs/Web/CSS/minmax()
