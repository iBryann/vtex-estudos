# Dicas brabas

## Vtex selecionando template errado

* Após linkar o tema, verá que a página deu um erro. Isso pode estar acontecendo porque a Vtex não selecionou seu novo tema na configuração da página. Para resolver isso siga os passos abaixo:

    > Acesse o admin > CMS > Páginas > Na lista de páginas selecione a edição da Home > Procure a seleção de template padrão > selecione seu tema.


## SafeData
Galera, sempre que precisarem consultar ou editar informações de usuários utilizem o SafeData para garantir a segurança dessas informações sensíveis (LGPD tá ai, em!). Basicamento o SafeData só permite que uma informação seja consultada pelo dono dela. Ou seja: o usuário precisa estar logado e mesmo assim só conseguira consultar uma informação no banco se for o proprietário.

[Clique aqui para aprender mais sobre o SafeData!](https://developers.vtex.com/vtex-developer-docs/docs/vtex-safedata)

Ah! As vezes pode acontecer de você estar usando a API antiga e querer passar a usar a API do SafeData e dar erro na resposta. Provavelmente você tá deslogado, tá tentando consultar uma informação que não te pertence ou só colocou o link errado. Abaixo os links de consulta das API's. Uma delas vai funcionar.

```js
// Método antigo
fetch('/api/dataentities/CL/search?email=<SEU EMAIL>&_fields=firstName')
.then(r => r.json())
.then(r => console.log(r))

// Metódo SafeData 1
fetch('/safedata/CL/search?email=<SEU EMAIL>&_fields=firstName')
.then(r => r.json())
.then(r => console.log(r))

// Metódo SafeData 2
fetch('/api/io/safedata/CL/search?email=<SEU EMAIL>&_fields=firstName')
.then(r => r.json())
.then(r => console.log(r))
```
