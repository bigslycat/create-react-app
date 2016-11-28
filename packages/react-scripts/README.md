# react-scripts-custom

It is a fork of [react-scripts](https://www.npmjs.com/package/react-scripts) package, which allows
you to make an injection of your custom settings in the webpack or replace Babel settings. Fork had
to do after the maintainer of
[Create React App](https://github.com/facebookincubator/create-react-app) package rejected this
[PR](https://github.com/facebookincubator/create-react-app/pull/1103). This package contains all the
changes of react-scripts from version to version.

This package is contained in
[react-scripts-custom branch](https://github.com/bigslycat/create-react-app/tree/react-scripts-custom)
of main repo [fork](https://github.com/bigslycat/create-react-app).

## Examples

Start with `create-react-app`
```
npm install --global create-react-app
create-react-app my-app --scripts-version react-scripts-custom
```

Start without `create-react-app`
```
npm install --global create-react-app
```

In `package.json`:

```json
{
  "scripts": {
    "start": "BABEL_REPLACE=.custom.babelrc WEBPACK_MERGE=custom.js react-scripts-custom start",
    "build": "BABEL_REPLACE=.custom.babelrc WEBPACK_MERGE=custom.js react-scripts-custom build",
    "test": "react-scripts-custom test --env=jsdom",
    "eject": "react-scripts-custom eject"
  }
}
```

Supported env variables:

-   `BABEL_REPLACE` — Replace Babel config
-   `WEBPACK_MERGE` — Merge your webpack cinfig to preinstall webpack config
-   `WEBPACK_REPLACE` — Replace webpack config

## Original readme

This package includes scripts and configuration used by [Create React App](https://github.com/facebookincubator/create-react-app).  
Please refer to its documentation:

* [Getting Started](https://github.com/facebookincubator/create-react-app/blob/master/README.md#getting-started) – How to create a new app.
* [User Guide](https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md) – How to develop apps bootstrapped with Create React App.
