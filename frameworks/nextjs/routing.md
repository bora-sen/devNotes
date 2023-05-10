# Routing

## How does Routing works ?

Next.js uses **folders** as routing.

![Routing](https://nextjs.org/_next/image?url=%2Fdocs%2Flight%2Fterminology-component-tree.png&w=3840&q=75)

### What is **app** directory ?

App Router is new, added in version 13. App folder built on React Server Components, you can handle loading, error states etc.

You can use app directory alongside with pages directory. They thought of old versions. 

* **In app directory**, every component is **[Server Component](server-components.md)** by default.
* You can create **[Client Components](client-components.md)** as well. ([How do you specify component to run on client side ?](client-components.md))

#### There are special files to run on specific conditions, what are they ?

**Note** : You can also use .jsx / .ts / .tsx file extensions for these files.

- **[page.js](./pages)** : Create unique UI for public page.
	- **[route.js](route.js.md)** : Create API-End Point for parent folder.
- **layout.js** : This is a interesting file, it wraps a page or child components for shared UI.
- **loading.js** : Create error UI, and this component is rendered when Next.js catches error.
- **not-found.js** : It renders when notFound action is thrown within a route segment.

### Component Hierarchy

You need to put these components in a hierarch.

- layout.js
- template.js
- error.js
- loading.js
- not-found.js
- page.js **or** nested layout.js

![Hierarchy](https://nextjs.org/_next/image?url=%2Fdocs%2Flight%2Ffile-conventions-component-hierarchy.png&w=3840&q=75)

You can use Stylesheet files btw.

![Nested Files](https://nextjs.org/_next/image?url=%2Fdocs%2Flight%2Fcomponent-collocation.png&w=3840&q=75)


**app directory uses Server-Centric Routing**

### What is Server-Centric Routing ?

This routing method is used when you want to align with server-side components and server-side data fetching. 

## Partial Rendering

### What is Partial Rendering ?

In partial rendering, when client visits the sibling routes, Next.js only renders the components that changed in component. It **will not** re-render or re-fetch data above the sub-tree.
You can create layout and inside this layout, you can re-render or re-fetch data only when required.

![partial-rendering](https://nextjs.org/_next/image?url=%2Fdocs%2Flight%2Fpartial-rendering.png&w=3840&q=75)

With server-side rendering, this is a very good performance-saving functionality. Because app renders or fetches components only when required.

[How can you use pages ?](pages.md)