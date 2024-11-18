
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
import React, { StrictMode } from 'react';
import ReactDOM from 'react-dom/client';

// Renderizando la aplicación envuelta en StrictMode
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <StrictMode>
    <MyComponent />
  </StrictMode>
);

```
>[!WARNING]
> In the production environment, to disable this behavior!







