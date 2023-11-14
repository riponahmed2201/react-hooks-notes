# All React Hooks Explain

- useState Hook
- useEffect Hook
- useRef Hook
- useCallback Hook
- useMemo Hook
- useContext Hook
- useReducer Hook
- useDebugValue Hook
- useDeferredValue Hook
- useId Hook
- useImperativeHandle Hook
- useInsertionEffect Hook
- useLayoutEffect Hook
- useSyncExternalStore Hook
- useTransition Hook

# useState Hook

This hook allows you to store and change information within a component. It returns a pair of the current state, a function that lets you update it and the value of the state

`Example`

```js
const [stateVariable, setStateVariable] = useState(initialValue);
```

# useEffect Hook

This hook lets you perform side effect like data fetching, updating the DOM, or subscribing to events.

`Example`

```js
useEffect(() => {
  // Side effect code here

  return () => {
    // Cleanup code (optional)
  };
}, [dependeencies]);
```

# useRef Hook

This hook lets you reference a value in your component. It doesn't cause the component to re-render when it changes and it remembers its value even after the component re-renders.

`Example`

```js
const myRef = useRef(initialValue);
```

# useCallback Hook

This hook is used to memorize (remember) functions, so you dont't have to recreate it every time your component re-renders, unless something it depends on changes.

`Example`

```js
const memorizedCallback = useCallback(callbackFunction, dependencies);
```

# useContext Hook

React Context is a way to manage state globally, It helps you pass data around components without having to manually pass it through props.

`Example`

```js
import React, { createContext, useContext } from "react";

const MyContext = createContext();

const ParentComponent = () => (
  <MyContext.Provider value="Hello from context!">
    <ChildrenComponent />
  </MyContext.Provider>
);

const ChildrenComponent = () => {
  const contextValue = useContext(MyContext);

  return <p>{contextValue}</p>;
};
```

# useReducer Hook

This hook is used for managing complex state logic that involves multiple sub-values or when the next state depends on the previous one.

`Example`

```js
const [state, dispatch] = useReducer(reducerFunction, initialArg, initFunction);
```

# useMemo Hook

This hook remembers the result of a function and only re-calculates if the inputs change.

`Example`

```js
const cachedValue = useMemo(calculateValue, dependencies);
```

# useDebugValue Hook

This hook allows developers to add a label or description for custom hooks, it help developers understand the purpose and usage of custom hooks when inspecting components in browser developer tools

`Example`

```js
useDebugValue(value, format);
```

# useDeferredValue Hook

This hook allows you to postpone a value change that might cause a component to lag during rendering.

`Example`

```js
const defferredValue = useDeferredValue(value, option);
```

# useId Hook

This is a custom hook that generate unique IDs within a React component.

`Example`

```js
const Id = useId();
```

# useImperativeHandle Hook

This hook allows you to control what is returned by a ref prop, specifically the ref handle.

`Example`

```js
useImperativeHandle(ref, createHandle, dependencies?);
```

# useInsertionEffect Hook

useInsertionEffect is a custom hook that allows you to insert the styles before any layout effects fire

`Example`

```js
useInsertionEffect(setup, dependencies?);
```

# useLayoutEffect Hook

This hook is similer to useEffect, but it runs after all DOM mutations are complete. This makes it useful for reading layout from the DOM and synchronizing state.

`Example`

```js
useLayoutEffect(() => {
  // Do something and either return undefined or a cleanup function

  return () => {
    // Do some cleanup code
  };
}, [dependeencies]);
```

# useSyncExternalStore Hook

useSyncExternalStore is a React Hook that lets you subscribe to an external store.

`Example`

```js
useSyncExternalStore(subscribe, getSnapshot, getServerSnapshot);
```

# useTransition Hook
useTransition is a React Hook that lets you update the state without blocking the UI

`Example`

```js
const [isPending, startTransition] = useTransition();
```