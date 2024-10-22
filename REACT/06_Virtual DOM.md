In normal code in browser if something gets changed whole page will get reloaded 
But in case of React there is a method **.createElement** which will create a ==Virtual DOM== which is used to compare with the ==Original DOM== and changes only the different parts hence the reloading part is avoided here

To optimize this process UI shouldn't be updated for every change instead there is an algorithm (fiber) which waits a few minutes and then updates the UI

**REACT FIBER** [Click here](https://github.com/acdlite/react-fiber-architecture)

**RECONCILIATION**
	The algorithm React uses to diff one tree with another to determine which parts need to be changed.

**UPDATE**
	A change in the data used to render a React app. Usually the result of `setState`. Eventually results in a re-render.

- Different component types are assumed to generate substantially different trees. React will not attempt to diff them, but rather replace the old tree completely.
- Diffing of lists is performed using keys. Keys should be "stable, predictable, and unique."
- When React updates the UI, it compares the current and previous versions of the virtual DOM (a process called reconciliation). For arrays of elements, React uses keys to identify which items have changed, been added, or removed.
- Keys help React distinguish elements in the list and decide how to update the UI. If keys are not provided, or if the keys are not unique, React might have to unnecessarily re-render the entire list or make inefficient updates.