![[Pasted image 20241016212218.png]]

We have to pass the props to every sub elements manually or components to make it accessible to the chosen component (Prop drilling).
What if we have a global scope where we keep the variables and use it in any files directly this is the concept of context API.

cant we keep a file for all the global variables and use it in the project?
- **File-based approach**: If you alter the variables in the file(mimicking context api), the updated values won't automatically trigger re-renders in React components that rely on those values.
- **Context API**: When you update the values in the context, React components subscribed to that context will automatically re-render and reflect the changes.

Context API is only dedicated for REACT. no need to install anything new it is inbuilt with react
the same problems arises in many other libraries hence a state management library is required i.e REDUX, REDUX - toolkit.
Redux helps in passing these data in an organized way.

- context is created using createContext 
- a context provider has to be provided or wrapped to all the elements that are going to use the elements in the context.
ex:- here a context provider is created 
```
const userContextProvider = ({children})=>{
	const [user,setUser] = useState(null);
	return(
		<userContext.Provider value={user,setUser}>
		{children}
		</userContext.Provider>
	)
}
export userContextProvider
```
- this created context provider has to be wrapped inside the elements generally is wrapped in `app.jsx` or `main.jsx` 

**HOW TO SEND THE DATA:**
	`const {setUser} = useContext(userContext);`
	now set the user using `setUser`.
**TO GET THE DATA:**
	`const {user} = useContext(userContext);`
	now we can use user directly which comes from the context.

**ANOTHER FORM:**
	
	export const ThemeContext = createContext ({ 
		themeMode: "light", 
		darkTheme: () =>{ }, 
		lightTheme: () =>{  }) 
		
		export const ThemeProvider = ThemeContext.Provider 
		
		export default function useTheme (){
			 return useContext (ThemeContext)
		}

```
<ThemeProvider value={light}>
	<App/>
</ThemeProvider >
```


