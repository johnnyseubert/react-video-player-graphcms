`npm create vite@latest`

---
`npm i`

---

`npm install tailwindcss postcss autoprefixer -D`

---

`npx tailwindcss init -p`

---

`npm i @apollo/client graphql`

---

Dentro do `tailwind.config`

---

```js
content: [
   './src/**/*.tsx'
],
```

---

Criar um arquivo global.css e importar no main.tsx

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```
---

`DICA`: Caso queira criar classes ou estilizar itens do css pode utilizar o tailwind no css

```css
body{
   @apply bg-zinc-900 text-zinc-100;
}

.title{
   @apply text-5xl;
}
```


---

# GraphQL

* `query` = Buscar Dados
* `mutation` = criar, alterar, deletar dados

* ``graphcms`` = interface gratuita para criar apis com graphql

### Sintaxe
```graphql
query{
   lessons{
      id
      name
      title
   }
}
```

---


`Criar uma instancia do ApolloClient`

```ts
import { ApolloClient, InMemoryCache } from "@apollo/client";

export const client = new ApolloClient({
   uri: 'LINK DA API DO GRAPHCMS ou GRAPHQL',
   cache: new InMemoryCache()
});
```

---

`npm install date-fns`

Biblioteca para trabalhar com datas muito completa