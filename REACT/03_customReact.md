**Injecting the custom component or tag to the root or main container**
```
function customRender (reactElement, container){ 
const domElement = document.createElement (reactElement.type) 
domElement.innerHTML = reactElement.children 
for (const prop in reactElement.props) { 
if(prop === 'children') continue; 
domElement.setAttribute(prop, reactElement.props[prop]) 
container.appendChild (domElement)
}
```

**creating a custom element  ==tree Structure==**
```
//tree structure
const reactElement = {
	type: 'a',
	props: {
		href: 'https://google.com', 
		target: '_blank' 
	}, 
	children: 'Click me to visit google' 
}
const mainContainer = document.querySelector('#root') 
customRender(reactElement, mainContainer)  //calling the function
```

now while creating a component we return jsx REACT does'nt understands this jsx it simply converts that jsx into a tree structure like mentioned above by a method called parsing

Now instead of <App /> we can also write App() because ==App== is nothing but a function.

The code that has been written is custom react and i have written the custom code to render it so it doesn't work if we directly use it in the react.

We have to define a separate tree that react understands i.e according to its standards. in another words syntax is not correct.

**Creating a react tree according to its own tree structure**
```
const reactElement = React.createElement ( 
'a', 
{href: 'https://google.com', target: '_blank' }, 
'click me to visit google' 
//whatever variable present can be put here
)
ReactDOM.createRoot(document.getElementById('root')).render(
	reactElement
)
```
**NOTE: In javascript inside an object we cannot use if statement this thing stops us from using conditionals inside the return element. Only evaluated expression is allowed.**

Babel converts JSX into standard JavaScript using `React.createElement()` calls.





