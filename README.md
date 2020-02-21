# Simple Node.js API

Simple Node.js API for workshop

Start by initializing Node.js package.

- Create your project folder and navigate to it.

```sh
yarn init
```

It will ask some questions from you.

- Give the new package information.

This will create a `package.json` inside your folder.

We are going to use [express.js](https://expressjs.com/) package which is created to simply creating APIs in Node.js.

Let's install our first dependency.

```sh
yarn add express
```

* Add gitinore file to ignore `node-modules` folder. [example](http://gitignore.io/api/node). 

* Create `index.js` file to start working on server. Add following to your `index.js`.

```es6
// index.js
const express = require('express');

const setupServer = () => {
  const app = express();
  const port = 3000;

  app.get('/', (req, res) => {
    res.send('Hello Wold!');
  });

  app.listen(port, () => {
    console.log(`listening on port ${port}`);
  });
};

setupServer();
```

* Run the file using 

```sh
node index.js
```

Test server visiting [http://localhost:3000](http://localhost:3000)

* Fix typo and refresh again to test.

* Install nodemon as devDependacy

```sh
yarn add -D nodemon
```

* create `nodemon.json` add below content.

```json
{
  "watch": ["*.js"]
}
```

* Let's add npm script to run it. Open your `package.json` and add following to it.

```json
"scripts": {
    "dev": "nodemon",
    "start": "node index.js"
  },
```

* Now to run

```
yarn dev
```
