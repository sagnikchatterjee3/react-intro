1. React;s component architecture allows us to create a reusable component to avoid messt ,duplicated code.
2. We use props to pass the value to each square from the parent compoent down to its child component.
```jsx
    function Square({value}) {
        return <button className="button">{value}</button>
    }
```
3. Props names should be the same as that is passed into the component.

