**WHY HOOKS :**
* assume there is a variable in a page and they are present in many places now if you want to update the variable in every location u have to select every tags and then alter it (here pure js is referred)
* In react we can update the values everywhere using the useState

**assume there is a variable and it has to be updated whenever we press a button**
u think this can be possible using classic js but the change will not reflect in the UI 
**REASON :-**
	In React, when you update a variable directly without using the `useState` hook, React doesn't detect the change and thus doesn't re-render the component. React relies on state to know when something has changed so it can trigger a re-render and update the UI. Without `useState` (or other state management solutions), React has no way of knowing that it needs to re-render, because it's not aware of the changes to regular variables.

The `useState` hook ensures that changes to the state trigger re-rendering of the component, which is why it's necessary for reflecting changes in the UI.

**REACT CONTROLS UI UPDATION**



