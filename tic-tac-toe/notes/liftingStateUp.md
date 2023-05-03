## Lifting State Up:

1. Currently, each Square component maintains a part of the game's state. To check for a winner in a tic-tac-toe game, the Board would need to somehow know the state of the each of the 9 Sqaure components.

2. Best approach is to store the game's state in the parent Board component instead of in each Square. The Board component can tell each Square what to display by passing a prop, like we did when we passed a number to each Square.

3. Lifting State Up:
   1. For collecting data from multiple children, or to have 2 child components communicate with each other, declare the shared state in their parent component instead. 
   2. The parent component can pass that state back down to the child via props. 
   3. This keeps the child component in sync with each other and with their parent.

4. Lifitng state up is common when React component are refactored.

5. Each square will now recieve a value prop that will be either be 'X', '0' or null for empty squares. The App component now maintains which squares are filled. Since state is private to a component that defines it, we cannot directly update the Board's state from Square , instead we will pass down a function from the Board's component to the Square component, and well have Square call that function when a square is clicked. 

6. handleClick(0) call will be part of the rendering the board component. Because handleClick(0) alters the state of the board component by calling setSqaures , our entire board component will be re-rendered again -> but this runs handleClick(0) again, leading to an inf loop.

7. Don't wanna call handleClcik until the user clicks.
8. 