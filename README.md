# All React Hooks Explain

- useState Hook
- useEffect Hook
- useRef Hook
- useCallback Hook
- useMemo Hook
- useContext Hook
- useReducer Hook
- useDebugValue
- useDeferredValue
- useId
- useImperativeHandle
- useInsertionEffect
- useLayoutEffect
- useSyncExternalStore
- useTransition

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
}, [dependeencies];
```
