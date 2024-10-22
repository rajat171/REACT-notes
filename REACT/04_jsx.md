in a component we return the html combined with javascript it is called jsx

```
function App(){
	name = "Rajath"
return(
	<>
		<Chai />
		<h1>here we can return html{name}</>
	<>
)
}
```
**NOTE: Inside the return we have to only include ==html and evaluated expression(here name)==**
javascript is written before return or outside the function. reason is mentioned in [[03_customReact]]
