Props enables us to reuse the components
we pass component as``<App />``
while calling this component we can pass some props like ``<App name="rajath" /> ``
						or
```
let myObj = { 
	username: "hitesh", 
	age: 21 
} 
return( 
 <Card channel="chaiaurcode" someObject={myObj} />
 )
```
**inside a component all of this will be accessible in props object**
```
function Card(props){
return(
	<>
	<h1>{props.channel}</h1>
	<h1>{props.someObject.username}</h1>
	</>
)
}
```

**Could also de-structure the object and use (to avoid using .props every time)**
```
function Card({channel,someObject}){  ******************
return(
	<>
	<h1>{channel}</h1>
	<h1>{someObject.username}</h1>
	</>
)
}
```




**Can also pass default value if the props is not at all passed during the use of component**
```
function Card({channel="raj",someObject}){   *****************
return(
	<>
	<h1>{channel}</h1>
	<h1>{someObject.username}</h1>
	</>
)
}
```