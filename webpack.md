# webpack

- It is a static module bundler for modern JavaScript applications.
- When webpack processes your application, it internally builds a dependency graph from one or more entry points and then combines every module your project needs into one or more bundles, which are static assets to serve your content from.

**Why webpack ?**

- To understand why you should use webpack, let's recap how we used JavaScript on the web before bundlers.
  There are two ways to run JavaScript in a browser. First, include a script for each functionality; this solution is hard to scale because loading too many scripts can cause a network bottleneck. The second option is to use a big .js file containing all your project code, but this leads to problems in scope, size, readability and maintainability.

**Advantages of using webpack**
\_ It speeds the development journey :

- If we are using webpack then your page does not need to reload fully on having a small change in javascript. This same benefit can
  be accessed for CSS if we will use loaders. - It also reduced the load time of the website during debugging and because of this, our time can be saved.

\_ It removed the problem of overwriting the global variables :

- We all know that webpack provides a module system that is based on ECMAScript(ES6).Every file that you will create here will become a module. Hence every variable that you will create in this file will be in the local scope.The problem of overwriting of global variables that we were facing will be solved.

\_ It provides splitting of code :

- Since it supports a module system that’s why files will be treated as modules hence we can use one file’s features into another.
  Despite having different files, we can access the same benefit. So it actually helps us in splitting our code into different modules.

  \_ It provides Minification :

  - Minification means minimizing the code without changing its functionality. It removes all the whitespace, line breaks that are consuming spaces. It also removes unnecessary code and changes the long variable names. So doing this reduces file size and minimizes the code.

  \_ It supports feature flagging :

  - Feature flagging is a software engineering approach by which we send code to different environments during feature testing.
    So webpack not only helps in development, it helps in testing as well.

    \_ Tree Shaking :

    - Webpack supports tree shaking, a process that eliminates dead code from the final bundle. This means that unused code or modules will not be included in the production build, resulting in a smaller bundle size.

    \_ Dynamic Imports: :

    - With dynamic imports, Webpack allows you to load modules asynchronously when needed. This can improve the initial page load time by only fetching the necessary code when a specific feature is accessed.

    \_ Code Analysis and Profiling :

    - Webpack provides tools for code analysis and profiling, helping developers identify bottlenecks and optimise their applications.
      This is crucial for achieving optimal performance and ensuring a smooth user experience
