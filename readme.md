# This setup provides a basic understanding of configuring react app with webpack

- This is a very minimal setup created solely for the purpose of learning how a react app could be configured without using build tool like `create-react-app`, `vite`
- As I got curious on how stuff happens behind, this got me cleared a lot of questions
- You can refer [this great article](https://www.freecodecamp.org/news/an-intro-to-webpack-what-it-is-and-how-to-use-it-8304ecdc3c60/?utm_source=pocket_mylist) to follow the guide, but as the code was outdated, I had to figure things out, and you might probably too
- The steps I have followed from the guide are same except from the app folder structure, which plays an important role in messing things up in your config at your first try

## Pre-requisites:
- basic understanding of how JS works in a browser, and in node
- knowing what is [**npm**](https://www.freecodecamp.org/news/what-is-npm-a-node-package-manager-tutorial-for-beginners/?utm_source=pocket_mylist) (node package manager)
- understanding of [**modules**](https://javascript.info/modules-intro?utm_source=pocket_mylist) in js
- installed latest node

## Steps:
- Initialize the project. It will create a `package.json` file
  - `npm init`
- Install the **dependencies** (packages which are required for running the project)
  - `npm i react react-dom`
- Install the **devDependencies** (packages which are required for developing and building the project). Make sure to use **`--save-dev`** flag.
  - bundler devDependencies :
    - `npm i webpack webpack-dev-server webpack-cli html-webpack-plugin --save-dev`
  - transpiler dependencies :
    - `npm i babel-core babel-loader @babel/preset-react @babel/preset-env --save-dev`
- You can check the `package.json` file updates on each install automatically as node handles that
- Setup the `webpack.config.js` file.
  - The article mentioned above gives a clear explanation of the config.
  - In my setup, I have tweaked some paths and added a new property `devtool` for [source maps](https://survivejs.com/webpack/building/source-maps/?utm_source=pocket_mylist)
  - source maps are great for debugging and are enabled by default on `create-react-app`
- Setup an `index.html` file with a `<div id=root></div>` inside `<body></body>`
- Setup some react code: `index.js` & `App.js`
- Add the necessary scripts in the `package.json`
  - the article also gives a good explanation on this
- PLAY AND TINKER...