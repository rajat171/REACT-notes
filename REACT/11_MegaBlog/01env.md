env variables has to be in the root directory of the project.

sensitive information are stored in .env files and this file is added into `gitignore` file.

There are some rules in defining the variables in .env files like start with`REACT_APP` or `VITE_` it purely depends on which type the application is created whether it is in `create react app` or `npm create vite@latest` or using express all these different application has different rules to define and access the .env files.

normally in production we use a config file to import the .env variables where we import and export the variables . we use this because we can directly use the string version of the whatever output we have got 