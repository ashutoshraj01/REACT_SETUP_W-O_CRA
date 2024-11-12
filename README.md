# React_Setup_Without_CRA

Setting up react application without using create react app(cra).

## Steps

1. Install Node.js in your system and make sure its installed by typing 'node -v' in your terminal.
2. Create a project folder of any name and navigate to the folder and then use 'npm init' to create a package.json file inside the folder. Navigate to the folder.

3. **webpack**
   [Know More](https://github.com/ashutoshraj01/REACT_SETUP_W-O_CRA/blob/main/webpack.md)

   - Install webpack dependencies

     `npm i --save-dev webpack webpack-cli webpack-dev-server`

   * **webpack** — Will allow us to bundle all of our code into a final build.
   * **webpack-cli** - CLI tool for providing a flexible set of commands for developers to increase speed when setting up a custom webpack project.
   * **webpack-dev-server** - Webpack dev server is a mini Node.js Express server.It uses a library called SockJS to emulate a web socket. Will enable us to create a localhost dev environment.

4. **Babel**
   [Know More](https://github.com/ashutoshraj01/REACT_SETUP_W-O_CRA/blob/main/Babel.md)

   - Install babel dependencies

   `npm i --save-dev babel-loader @babel/preset-env @babel/core @babel/plugin-transform-runtime @babel/preset-react @babel/eslint-parser 
@babel/runtime @babel/cli`

- **babel-loader** - Allows transpiling JavaScript files using babel and webpack. exposes a loader-builder utility that allows users to add custom handling of Babel’s configuration for each file that it processes.
- **@babel/preset-env** - Allows you to use the latest JavaScript without needing to micromanage which syntax transforms (and optionally, browser polyfills) are needed by your target environment(s). This both makes your life easier and JavaScript bundles smaller!
- **@babel/core** - Main package.
- **@babel/plugin-transform-runtime** - A plugin that enables the re-use of Babel’s injected helper code to save on codesize.
- **@babel/preset-react** - use react preset when we are using Reactjs. Helps in converting html files to react based file.
- **babel-eslint** - Parser that allows ESLint to run on source code that is transformed by Babel.
- **@babel/runtime** - Package that contains a polyfill and many other things that Babel can reference.
- **@babel/cli** - Command line to use babel.

5. **Linters**
   [Know More](https://github.com/ashutoshraj01/REACT_SETUP_W-O_CRA/blob/main/Linters.md)

   - Install required Linters and path

   `npm i --save-dev eslint eslint-config-airbnb-base eslint-plugin-jest eslint-config-prettier path`

6. **React & React Dom**

   - The ReactDOM in React is responsible for rendering the elements or Components in the actual DOM of the web page. It is a package in React that provides DOM-specific methods that can be used at the top level of a web app to enable an efficient way of managing DOM elements of the web page. ReactDOM provides the developers with an API containing the various methods to manipulate DOM.

   - Install react and react-dom
     `npm i react react-dom`

7.
