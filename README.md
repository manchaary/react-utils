### React utility functions

1. `useStore` - React `useContext` wrapper. Throw an error if Context is empty.

Example:
```
const { loadData } = useStore(MyStoreContext);
```

2. `useOutsideClick` - Click outside of defined `ref` (used for closing dropdowns, modals). Removes listener when `open` is false.

Example:
```
const ref = useRef(ref)
const [open, setOpen] = useState(false);
const closeHandle = () => setOpen(false);
useOutsideClickClose(open, ref, closeHandle);

return (
  <div ref={ref}>...</div>
);

```

3. `createProvider` - Creates provider component and context for mobx stores.

Example:

```
const { Context, Provider } = createProvider(MyMobxStore);
```