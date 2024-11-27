# TIL : `useState()`

_27-11-2024_

>[!Note]
El `state` es una variable que puede ser modificada de manera dinámica y perdura entre renderizaciones


👉 [watch here](https://www.youtube.com/watch?v=GMnWXlJnbNo&t=7482s)

You should know 3 things first:

1. It will mount the component (this is why we see 0 on the screen — because `useState(0)` is initializing with 0. It is rendering for the first time).
2. User interaction will change the state of the component.
3. An async event (like an API call, for example) can also trigger state changes or side effects.


```tsx

import { useState } from 'react';
import { Button } from './components';
import './App.css'

function App()
{
  const [count, setCount] = useState(0);
  const countMore = () => {
    setCount((count) + count + 1);
  }
  return (
  <>
    <Button label={`Count is ${count}` parentMethod={countMore} />
  </>
  )
}

export default App
```

How works ...`const [count, setCount]`
 
- React utiliza desestructuración de arrays para este patrón [ o, o]
- `count`: Representa el valor actual del estado.
- `setCount`: Es una función que cambia el valor del estado y reactualiza el componente cuando el estado cambia.
`useState(0);` El número 0 es el estado inicial de la variable count.


>[!NOTE]
`useState` is key in functional components because it lets you manage state without the need for classes. 😎

