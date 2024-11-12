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
