
# Configuration File Information

---
title: 'Configuration Information'

author: 'Hima 'Dionysus' Balde'

date: 2021/12/29

description: React App w/ custom WP configs and CSS

tag: web dev, jsx, tsx, mdx

---

...
\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\

## CSS DESIGN

> `CSS-loader`

1. _allows use of import Styles from './styles.css'_ or
2. _import { style1, style2 } from './styles.css'_

```html
<div className={Style.style1}> 1. Hello World</div>
```

```html
- <div className={style1}> 2. Hello World </div>
```

- _or (3) with the destructuring syntax_
  - can write css rules via: .home-button {...} ex.

```jsx
> import { homeButton } from './styles.css'
```

> run `npm install` --save package-name or `yarn add` package-name to save a lib as a dep (as opposed to a devdep)

- use default imports/exports if the module has 1 component
- use named exports wj/ utility mods exporting multiple func
- can only have one default exp. but several named exp.

\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\

...

...

## WEBPACK config file

```jsx

module.exports = {
    plugins: [
    new HtmlWebpackPlugin({
        template: 'public/index.html',
        favicon: 'public/favicon.ico'
    })
    ],
};
"start": "webpack-dev-server"
```

\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\

### Package Descriptions

| ------------------------------------------------------------------------- |
| Packages Using in this Project | _____________________ **Description** |

- `react` `react-dom` `prop-types` `react-router-dom`

> `Babel`

- @babel/core  _main dep for Babel_ --transpiler--
- @babel/preset-env lets you code es '15-'17 & Babel  auto detect/transpile
- @babel/preset-react (ID that it's a react app)
- ~@babel/plugin-proposal-class-properties (Use class properties)~
- @babel/plugin-syntax-dynamic-import, _dynamic import/exports_

> `CSS`

- auto-prefixer, post-css-preset-env _css-modules_ _css-loaders_
- semantic-ui-react, reactstrap, tailwindcss
- html-webpack-plugin _pre-gen html doc w  temp or make your own_
- style-loader— Adds CSS to the DOM by injecting a < style > tag

> `WebPack`

- webpack _Module bundler_
- webpack-nano _Webpack CLI_
- webpack-plugin-serve _dev server via local_
- npm-run-all: _run several npm Rx concurrently or simul.._

| ----------------------------------------------------------------- |
\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
...

### `HUSKY` `LINT` `PRETTIER`

>Format code on commit

```bash
`npm install` --save husky lint-staged prettier
```

| ------------------------------------------------------------------ |
`husky` allows githooks to be used in similar way to npm scripts
`lint-staged` enables scripts to be run on git files that're staged
`prettier` JS formatter
| ------------------------------------------------------------------ |

...

1. `add` code to scripts section of package.json

    ```json
    "scripts": {
    "precommit": "lint-stage"
    }

    ```

2. Then add this code field to package

    ```json
    + "lint-staged": {
    +   "src/**/*.{js,jsx,json,css}": [
    +     "prettier --single-quote --write",
    +     "git add"
    +   ]
    + },
    ```

...