App-write is a backend as a service provider here app-write has some methods to access and write the data and other services has other syntax .
Now problem arises when we want to change the service from one to other like for example `appwrite to firebase` then we have to change the whole methods in the code hence we try to generalize these methods so that if we wanted to change the backend service we can only alter the methods. to do this we can use the classes and this classes is called as services.
From this the methods name will be same but by only changing the inside working of the function we can change the services anytime.

### Key Benefits:

- **Ease of switching**: You only need to change which service class you're using, not the entire backend interaction code.
- **Code reusability**: The common interface ensures that the same method names are used across services, promoting consistency and reusability.
- **Flexibility**: You can easily expand to support more services in the future by creating new service classes that follow the same structure.

```
async getCurrentUser(){
        try {
            await this.account.get();
        } catch (error) {
            console.log("AppWrite service :: getCurrentUser :: error",error);
        }
        return null;
    }
```
^^ here return null is used if try catch doesn't gets executed by any chance then it returns null

To understand better take a look into the `auth.js` file of the `MegaBlog` project where methods are created and we can access those methods using only `authservice.[methodName()]`.

Now this file is future proof i.e if we change the database service our task is to only change the function and not the whole frontend we just need to keep the attributes same that's it.