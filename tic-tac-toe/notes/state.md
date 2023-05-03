1. To make a component to "remember" that an event has just happened in it, and fill it with a value, component uses state.

2. React provides a special function called useState that we can call our component to let it "remember" things. 

```jsx 
    const [value,setValue] = useState(null);

```

3. value stores the value and setValue is a function that can be used to change the value. The null passed to useState is used as the initial value for this state variable,so value here starts off equal to null.

4. By calling the set function from an onClick handler, we are telling React to re-render that Suare whenever its \<button> is clicked. After the update, the Square's value will be X .


5. handleClick(0) call will be part of the rendering the board component. Because handleClick(0) alters the state of the board component by calling setSqaures , our entire board component will be re-rendered again -> but this runs handleClick(0) again, leading to an inf loop.

6. Don't wanna call handleClcik until the user clicks.

7. Now that our state is in the Board component, the parent board component passed props to the child Square components so that they can be displayed correctly. When clicking on a Square, the child Square component now asks the parent Board component to update the state of the Board. 

8. When the board's state changes, both the Board component and every child Square re-renders automatically. Keeping the state of all squares in the Board component will allow us to determine the winner in future.


