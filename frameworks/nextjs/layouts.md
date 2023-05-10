# Layouts

## How to define a Layout ?

You need to export default function from **layout.js** file. 

![placeholder](https://nextjs.org/_next/image?url=%2Fdocs%2Flight%2Flayout-special-file.png&w=3840&q=75)

This component accepts {children} prop, you can populate other layout components or render child components using {children} prop.

### Using **layout.js** 

```jsx
// app/dashboard/layout.jsx
export default function DashboardLayout({children}){
	return (
		<section>
			{/* You can include shared components (Header, Footer, etc.) */}
			
			<nav></nav>
			
			{children}
		</section>
	)
}
```

#### Also;
- Layouts can fetch data.

### Root Layout (Required!)

This layout is on **/app/layout.js** file, it's a initial layout file that containts html & body tags.

```jsx
// app/layout.jsx
export default function RootLayout({
  children,
}: {
  children: React.ReactNode,
}) {
  return (
    <html lang="en">
      <body>{children}</body>
    </html>
  );
}
```