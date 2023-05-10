# Pages

## How to definde a Page ?

You need to export a component from **page.js** file inside the app directory.

![placeholder](https://nextjs.org/_next/image?url=%2Fdocs%2Flight%2Fpage-special-file.png&w=3840&q=75)

Inside this file, it's a simple React.js component.

```jsx
// `app/page.js` is the UI for the root `/` URL
export default function Page() {
  return <h1>Hello World</h1>;
}
```

- You can use .jsx / .ts / .tsx file extensions.
- This **page.js** file is required in order to access this page publicly.
- This is a **[Server Component](server-components.md)** by default. But you can specify to make this component **Client Side** ([How to specify a component to make it Client Side ?](client-components.md))
- Because it's a **Server Side Component by default**, you can fetch data.



[Routing](./routing.md)