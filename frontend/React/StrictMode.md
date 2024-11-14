
## What I Learned :LiGlasses:
---
It manages how the components work.

How StrictMode works:

1. It creates a component.

2. Renders that component.

3. Destroys that component.

4. Reload the same component again.

5. Check if the state of the component that was just recreated is the same as before it was destroyed.
## Example :LiCode2:
---
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

## Notes and Reflections :LiNotebookPen:
---
**If you call an** `/api` endpoint, and you see that the component was created twice, that means `<StrictMode>` is working.
## References :LiLink2:
---

- [Link to source 1](#)
- [Link to source 2](#)




