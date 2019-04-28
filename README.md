# React From Scratch

TLDR of how to make a starter react project from scratch so we don't have a black box toolchain. This guide is no hand holding -- use it if you generally understand how project organization scaffolding works and how JS/Babel/Webpack work together.

## Prerequisites

- npm
- node

### Create a project directory

`mkdir react_from_scratch`

### Initialize node

`npm init`

### Make a general React project structure

In your project directory:

`mkdir public src`

`public` - houses static resources

`src` - JS source code

### Add `index.html` to your `public` static resources

```html
<!-- sourced from https://raw.githubusercontent.com/reactjs/reactjs.org/master/static/html/single-file-example.html -->
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
  <title>React Starter</title>
</head>

<body>
  <div id="root"></div>
  <noscript>
    You need to enable JavaScript to run this app.
  </noscript>
  <script src="../dist/bundle.js"></script>
</body>

</html>
```

### Install Babel

```
npm i @babel/core babel-loader @babel/preset-env @babel/preset-react --save-dev
```

Create `.babelrc` on the project root:

```json
{
  "presets": ["@babel/preset-env", "@babel/preset-react"]
}
```



