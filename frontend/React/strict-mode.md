
# TIL : `<StrictMode>` controls how the components function


How StrictMode works:

1. It creates a component.

2. Renders that component.

3. Destroys that component.

4. Reload the same component again.

5. Check if the state of the component that was just recreated is the same as before it was destroyed.

👉 [How StrictMode works - 📺 ](https://youtu.be/GMnWXlJnbNo?si=Z3BjJKEFp0oiyClO&t=3844)

> **If you call an** `/api` endpoint, and you see that the component was created twice, that means `<StrictMode>` is working.

## Example 

```jsx
import { StrictMode } from 'react';
import { createRoot } from 'react-dom/client';
import App from "./App.tsx";

const root = createRoot(document.getElementById('root')!);

// Renderizando la aplicación envuelta en StrictMode
root.render(
  <StrictMode>
    <App />
  </StrictMode>
);

```
>[!Note]
> The `!` is used to ensure that "root" is not `null`, avoiding potential issues if the DOM element with the `ID` `root` is missing.

>[!WARNING]
> In the production environment, to disable this behavior!







