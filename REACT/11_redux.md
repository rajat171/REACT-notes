<u>Redux</u> is a independent state management library

react-redux is used for redux in react

We import react and react-native to use react-native in the similar way we import redux as well as react-redux to use redux in react because redux is the core library so we have to take redux.

React-redux is basically a bridge so that we can use redux in react.

First this prop drilling related problem was attempted to solve by facebook using flux which is first version to redux and then redux is built 

Flux had better data flow than the context api for example in context api we used to spread the array and then update the value. what if i want to update the value and get the value similarly no need to spread and make changes keeping that in mind. Flux solved this problem but data flow was not still that great so

react had a conference where they introduced redux having some conditions on it like
- there should be only one store
- state should be only read only
- changes should be only made through the functions (here reducers).

In redux lot of configuration had to be done to setup the state and many things then some middlewares started to show on which tried to create these things later on redux included their own redux-toolkit which had abstraction where 
- store can be created very easily.
- and many more

# History ends here

**Store:** assume it as a global variable where things are stored .
	there should be a single store inside that store there can be many number of stores.
**reducers:** functions to update or insert the values into the store.
**useSelector:** function to read the value
**useDispatch:** function to write the value. it uses reducers to do this job

there are some set of rules/steps that has to be kept in mind to configure the store in redux

- configure store, used from react redux
- next we have to create reducers here it is called slice but before this be need define a initial state
- slice is like a bigger version of reducer, to create slice we use createSlice method which takes an object which has name, initial state, reducers(we have to provide the list of reducers and define it there itself)
- then we need to export the reducers this is a syntax these reducers are available in Slice.actions further when we need to access the reducers it will help
- at last we have to export all the reducers in group like todoSlice.reducer (here not individual)
- then provide reducers to the store
- to add the values to the store we need to use useDispatch, store and reducers are part of redux but the selectors and dispatcher can be got from react
- import useDispatch wherever we need to change the store and the most important part is ==useDispatch uses reducers to change the value in the state== we have to provide a reducer inside the dispatcher function 
- Now to get the access of the state we use useSelector which provides state in the callback function inside it `useSelector(state => state.todos)` 
- In context api we used to wrap up all the components in the provider similarly in here we have to do the same. we have to wrap all the possible components, we can wrap it wherever we want either App.js or main.js anyone will do. similar to context api we have to give value here it is state, for this exact reason we need to export the store at the beginning.
