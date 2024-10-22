can look into `npm` documentation to import the package 
`npm i uuid` 

![[Pasted image 20241016191212.png]]
dependencies
`devdependencies`

The `"scripts"` section in the `package.json` file is used to define custom commands
for ex: if i have to run a command which is huge. Now instead of typing the whole command we can assign that same command to a shorter one so that we dont have to enter whole command every time instead say `npm start` <-- just an example.

**Global packages:**
Installing a global package with NPM means that the package is available system-wide, not just in a specific project. It can be used from any location on your system, typically for command-line tools or utilities that you might need across multiple projects. just include -g before the package name to specify the package as global.
`npm install -g <package-name>` 