React creates a ==virtual DOM== and then compares that with the ==main DOM== and alters only that things which are different

in package.json file u will find ==react-scripts== this is responsible for injecting javascript file to the index.html file
But when u create react with vite the script file is directly loaded into the index file(classic) hence no need of the react-scripts.

```
ReactDOM.createRoot(document.getElementById('root')).render (
		<App />
		) 
```
 here the div is selected and <App/> component is rendered inside this root div

while returning a file everything should be wrapped in a single div or fragment(<></>) and the component name should start with capital letter