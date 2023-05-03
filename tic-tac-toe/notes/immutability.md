## Immutability and changing data 

1. In handleClick() we called .slice() to create a copy of the Squares array instread of modifying the existing array. 

2. There are 2 approached of chaning data:
   1. mutate the data by directly changing the data's values.
   2. replace the data with a  new copy which has the desired changes.

3. Benefits gained by not mutating:
   1. Makes complex features much easier to implement. Avoid direct data mutation lets us keep previous verisons of the data intact, and reuse them later.
   2. By default all child components re-render automatically when the state of a parent component changes. This includes even the child components that wernt affected by the change. Although re-rendering is not by itself noticeable to the user , we might want to skip re-rendering a part of the tree that clearly wasn't affected by it for performance reasons. 
   3. Immutability makes it very cheap for components to compare whether their data has changed or not .

4. 