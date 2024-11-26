# TIL : Export components

_26-11-2024_

# Don't ❌

📂
```less
src/
├── App.tsx
├── components/
│   ├── Button/
│   │   ├── Button.tsx
│   │   ├── Button.css
```

📄 `App.tsx`
```ts
import { Button } from './components/Button/Button';
```

# instead ✔️

📂
```less
src/
├── App.tsx
├── components/
│   ├── Button/
│   │   ├── Button.tsx
│   │   ├── Button.css  
│   ├── index.ts --------> Create an index that exports all the routes
```

📄 `index.ts`
```ts
export * from './Button/Button.tsx'; 
```


📄 `App.tsx`
```ts
import { Button } from './components'; // looks nice 💅


(...)
```


👉 [watch here](https://youtu.be/GMnWXlJnbNo?si=ggbtq6A5ScWf5agm&t=6877)
