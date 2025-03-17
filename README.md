# PLuzPitty
Inventory control system for stationery businesses to track stock, manage sales and purchases, and generate detailed reports. Built with modern web technologies [frontend: (React, tailwind), backend: (C# with Entity framework) and DB: SQLServer]

Getting Started
Prerequisites:
Node.js and npm installed
pnpm installed globally

To install pnpm, run:
- npm install -g pnpm

### 📦 Basic pnpm Commands
|  Command      |                      Description                      |
|---------------|-------------------------------------------------------|
| pnpm install  | Installs all dependencies.                            |
| pnpm add      | Adds a new package to the project.                    |
| pnpm remove   | Removes a package from the project.                   | 
| pnpm update   | Updates project dependencies to the latest version.   |
| pnpm run      | Runs a script from the package.json file.             |
| pnpm build    | Builds the project for production.                    |

Documentation [https://pnpm.io/installation]

### ⚛️ Basic React Hooks
1. useState - Manage component state
```jsx
    import { useState } from 'react';

    function Counter() {
    const [count, setCount] = useState(0);

    return (
        <div>
        <p>Count: {count}</p>
        <button onClick={() => setCount(count + 1)}>Increment</button>
        </div>
    );
    }
```

Manages state within functional components.
Re-renders the component when the state changes.

2. useEffect - Handle side effects

```jsx
import { useState, useEffect } from 'react';

function DataFetcher() {
  const [data, setData] = useState([]);

  useEffect(() => {
    fetch('/api/items')
      .then(response => response.json())
      .then(data => setData(data));
  }, []);

  return (
    <ul>
      {data.map((item) => (
        <li key={item.id}>{item.name}</li>
      ))}
    </ul>
  );
}
```
Executes code after the component renders.
Useful for data fetching, subscriptions, and manually changing the DOM.

3. useContext - Share state globally
```jsx
import { createContext, useContext } from 'react';

const UserContext = createContext();

function App() {
  return (
    <UserContext.Provider value="Alice">
      <User />
    </UserContext.Provider>
  );
}

function User() {
  const name = useContext(UserContext);
  return <p>Username: {name}</p>;
}
```
Shares data across multiple components without prop drilling.

React documentation [https://react.dev/reference/react]

### 🎨 Basic Tailwind Components
1. Button
```html
    <button class="bg-blue-500 text-white py-2 px-4 rounded">
    Click Me
    </button>
    2. Card
    html
    Copiar
    Editar
    <div class="max-w-sm rounded overflow-hidden shadow-lg p-4 bg-white">
    <h2 class="text-xl font-bold">Product Title</h2>
    <p class="text-gray-700">Description of the product.</p>
    </div>
    3. Input
    html
    Copiar
    Editar
    <input class="border border-gray-300 rounded p-2 w-full" placeholder="Enter text" />
```

Tailwind documentation [https://v2.tailwindcss.com/docs]

📝 License
This project is licensed under the MIT License.
