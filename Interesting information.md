* in ``onClick`` we have to give a function not a returned value
* ex: ``onClick = {setNumber()}`` this is not allowed because here we are executing the function
* now what if i want to pass an argument in the function 
* ``onClick = { ()=> setNumber(22)}``
