react doesn't have any inbuilt router we have to use a 3rd party library(react-router-dom)

**Link:**
	"a" tag reloads a page and redirects the page
	hence Link is used for react-router-dom here the page doesn't get reloaded.
	instead of "href" we use "to" inside the Link tag.

We use navlink from the router dom and specify the location

in the ```<App />``` or any other component we can render the page using router-dom gives 
```<RouterProvider router={router}/>``` which takes a router .We have to create router

**OUTLET:** when we want certain parts of the page to be static and some to be dynamic router DOM provides outlet where we can change things dynamically.

```
<Home />
<Outlet />   # Outlet is injected here before this we have to import Outlet
<Footer />
```



There are 2 ways to create router
1. 
```
const router = createBrowserRouter(
	{ path: '/', 
	  element: <Layout/>, 
	  children: [
	    { path: "",               # for '/'
	      element: <Home />
	      },
	    { path:'about',           # for '/about'
	      element:<About/>
	      }
	    ]
	}
```

2. 
```
	const router = createBrowserRouter ( 
		createRoutesFromElements (
			<Route path='/' element={<Layout />}> 
				<Route path='' element={<Home />}/> 
				<Route path='about' element={<About />}/> 
				<Route path='contact' element={<Contact />}/> 
			</Route>
		)
	)
```

**LOADER:**
