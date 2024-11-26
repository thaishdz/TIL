

# TIL: Staless vs Stateful

There are 2 types of components:

### Dummy components 🐵

_Delega la lógica a otro y lo usamos para estilizar algún componente_

```tsx
export const Button = ({label, parentMethod}: Props) => {
  return (
    <button className="custom-button" onClick={parentMethod}>
      {label}
    </button>
  )
}
```
This component does not manage any state. When we click the button, it calls the `parentMethod` function.
It’s considered a dummy component because it is stateless (does not have its own state).

---

### Smart components 🧠

_contiene la lógica de aplicación_

_... also called a stateful component_

How do I know that? Easy, it uses `useState()` 🐵 and it has logic.

```tsx
function App() {
  const[count, setCount] = useState(0)
  const countMore = () => {
    setCount((count) => count + 1)
  }
  return (...)
}

```
>[!NOTE]
A `state` is a place where variables, methods, and everything are stored, and then we can use them in JSX.


👉 [watch here](https://youtu.be/GMnWXlJnbNo?si=QBosqPJGBoCnNGBx&t=7315)
