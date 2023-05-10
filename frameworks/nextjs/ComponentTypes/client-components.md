#### What is a Client Component ? 
A component runs on **Client-Side** of Next.js App

#### How do you specify component to run on Client Side ?

```jsx
"use-client";

import {fancyComponent} from "fancy/component"

export function ClientComponent(){
	return (
		<div>CLIENT SIDE COMPONENT</div>
	)
}
```

You need to use **"use-client"** 