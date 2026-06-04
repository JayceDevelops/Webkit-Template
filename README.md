# Webkit-Template
A clean, minimal boilerplate template for setting up and configuring WebKit instantly within web development projects.


## Setting Up Webpack For Javascript
-------------------------------------

### Step One:
Within your newly made project run
```batch
npm init -y --init-type=module
```
This will create package.json & package-lock.json

### Step Two: 
Create a directory called src and then a file named index.js within the src folder
```batch
mkdir src && touch src/index.js
```
The index.js file is the root of all our javascript

### Step Three: 
In the root of the project so outside of src, create a file called webpack.config.js
```batch
touch webpack.config.js
```
This is the config file webpack uses for its configuration

### Step Four:
Within the webpack.config.js file copy and paste the following code:
```javascript
import path from "node:path";

export default {
  mode: "development",
  entry: "./src/index.js",
  output: {
    filename: "main.js",
    path: path.resolve(import.meta.dirname, "dist"),
    clean: true,
  },
};
```
