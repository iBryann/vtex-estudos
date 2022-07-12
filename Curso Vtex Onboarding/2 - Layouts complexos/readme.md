## Experiência

Super legal o flex-layout da Vtex. Não deixem de estudar a documentação desse componente, afinal nele tem muita coisa util como rowGap e colGap para colocar espaçamentos entre linhas e colunas.

https://developers.vtex.com/vtex-developer-docs/docs/vtex-flex-layout#flex-layout

Outro detalhe muito interessante para a organização do código é que contanto que os arquivos estejam dentro da pasta "store/blocks", podemos estruturas os arquivos e pastas como a gente preferir que a Vtex cosegue renderizar eles. Podemos até separar trechos grandes de código (como um slider ou um modal) em um arquivo separado e só referenciar ele pelo nome do bloco.


Por quê alguns seletores foram depreciados na Vtex
https://vtex.io/docs/releases/2019-week-43-44/css-selectors-deprecation?utm_source=toolbelt/


## Dicas brabas

Nessa seção, em cada etapa dos meus estudos, vou deixar algumas dicas de coisas interessantes que consegui absorver.

### 1. Como saber o ID de um departamento, categoria, subcategoria ou produto?

Se quiser de uma categoria, por exemplo, abra a página de uma categoria, atualize ela e abra o console. No console digite "__RUNTIME__.route.params". Vc receberá um objeto como o abaixo:

```js
{
    "id": "38",
    "department": "frios-e-laticinios",
    "category": "iogurtes"
}
```

Nesse caso, o ID em questão sempre se refere ao contexto no qual você está. Por exemplo: se estiver na página de um produto esse ID será do produto, mas se estiver em uma página de categoria esse ID será o da catiguria 😌