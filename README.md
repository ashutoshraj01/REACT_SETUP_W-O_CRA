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

5.  **Linters**
    [Know More](https://github.com/ashutoshraj01/REACT_SETUP_W-O_CRA/blob/main/Linters.md)

    - Install required Linters and path

    `npm i --save-dev eslint eslint-config-airbnb-base eslint-plugin-jest eslint-config-prettier path`

6.  **React & React Dom**

    - The ReactDOM in React is responsible for rendering the elements or Components in the actual DOM of the web page. It is a package in React that provides DOM-specific methods that can be used at the top level of a web app to enable an efficient way of managing DOM elements of the web page. ReactDOM provides the developers with an API containing the various methods to manipulate DOM.

    - Install react and react-dom
      `npm i react react-dom`

7.  Create folder called “public” in the root of the project. Inside that, create `index.html`.
8.  Create src folder and inside that create a file called App.js. Add the following code to it:
    `import React from "react";

        const App = () =>{
            return (
                <h1>
                    Welcome to React App thats build using Webpack and Babel separately
                </h1>
            )
        }

        export default App;`

9.  Create an index.js file at the root of project. This will act as entry point for our webpack.

10. Create a file called webpack.config.js at the root of project and add the following code. On a higher note, this file contains configs that takes care of bundling the files into one single file and setting up the dev server.

11. Create a file called .babelrc at the root.

12. Update package.json file

    - Add the start and build scripts to it.
    - The start script asks to run the webpack-dev-server in our current project at port 9500, from the public folder.
    - The build command asks us to build this package in main.js file. It actually runs all logic in webpack.config.js file.

13. Run `npm run build`. it generates main.js file in our public folder. The file is actually over 1 MB in size. This is our development build.

14. Start the application by giving `npm start` from terminal. This will start our dev server.

15. Now we can try changing it to production build. For this you need to make the following change to webpack.config.js file.
    `mode: "production"`

    - Now running npm run build will create main.js file again but the size will be very less (<200kb).
      With the optimization from 1000 KB to 200 KB, we might want to use production build always. But, we should use development mode while doing development because the hot reloading is faster in development mode.

16. HMR is handled by webpack-dev-server. We can use HMR without page load option too. Setting the required options helps greatly in performance aspect.

            `//If you want to use HMR but no live reload then use the below config in webpack.config.js
            devServer: {
                    hot: true ,
                    liveReload:false
                }

            //If you want don't want to use HMR but want to use live reload then,
            devServer: {
                    hot: false ,
                    liveReload: true
                },

            //If you want don't want to use live reload then,
            devServer: {
                    hot: false , //this is mandatory to be set to false for this
                    liveReload: false
                },`
