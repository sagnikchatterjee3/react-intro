1. To make a component to "remember" that an event has just happened in it, and fill it with a value, component uses state.

2. React provides a special function called useState that we can call our component to let it "remember" things. 

```jsx 
    const [value,setValue] = useState(null);

```

3. value stores the value and setValue is a function that can be used to change the value. The null passed to useState is used as the initial value for this state variable,so value here starts off equal to null.

4. 