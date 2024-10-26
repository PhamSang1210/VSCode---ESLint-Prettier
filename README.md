# VSCode - ESLint, Prettier & Airbnb Setup for Node.js Projects

Click Speed Heading

<ol>
    <li>
        <a href="#one">Install ESLint & Prettier extensions for VSCode</a>
    </li>
    <li>
        <a href="#two"> Install Packages</a>
    </li>
    <li>
        <a href="#three">Create .prettierrc for any prettier rules (semicolons, quotes, etc)</a>
    </li>
    <li>
        <a href="#four">Create .eslintrc.json file (You can generate with npx eslint --init)</a>
    </li>
</ol>

<h4 id="one">1. Install ESLint & Prettier extensions for VSCode</h4>

<p>Optional - Set format on save and any global prettier options</p>

<h4 id="two">2. Install Packages</h4>

```
npm i -D eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-config-airbnb-base eslint-plugin-node eslint-config-node -f
```

or

```
yarn add --dev eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-config-airbnb-base eslint-plugin-node eslint-config-node -f
```

<h4 id="three">3. Create .prettierrc for any prettier rules (semicolons, quotes, etc)</h4>

```
{
  "trailingComma": "es5",
  "tabWidth": 4,
  "semi": true,
  "singleQuote": true
}
```

<h4 id="four">4. Create` .eslintrc.json ` file (You can generate with npx eslint --init)</h4>

```
{
  "env": {
    "commonjs": true,
    "es6": true,
    "node": true
  },
  "extends": ["airbnb-base", "prettier", "plugin:node/recommended"],
  "globals": {
    "Atomics": "readonly",
    "SharedArrayBuffer": "readonly"
  },
  "parserOptions": {
    "ecmaVersion": 2018
  },
  "plugins": ["prettier"],
  "rules": {
    "prettier/prettier": "error",
    "no-unused-vars": "warn",
    "no-console": "off",
    "func-names": "off",
    "no-plusplus": "off",
    "no-process-exit": "off",
    "class-methods-use-this": "off"
  }
}
```

<h4 id="four">5.Package `npm init @eslint/config`</h4>

```
npm init @eslint/config
```

Answer:
? How would you like to use ESLint? ...
To check syntax only
To check syntax and find problems

-   [x] To check syntax, find problems, and enforce code style

? What type of modules does your project use? ...

-   [x] JavaScript modules (import/export)
        CommonJS (require/exports)
        None of these

? Which framework does your project use? ...
React
Vue.js

-   [x] None of these

? Does your project use TypeScript? » No / Yes -> No

? Where does your code run? ... (Press <space> to select, <a> to toggle all, <i> to invert selection)
Browser

-   [x] Node

? How would you like to define a style for your project? ...
Use a popular style guide

-   [x] Answer questions about your style

? What format do you want your config file to be in? ...

-   [x] JavaScript
        YAML
        JSON

? What style of indentation do you use? ...
Tabs

-   [x] Spaces

? What quotes do you use for strings? ...

-   [x] Double
        Single

? What line endings do you use? ...

-   [x] Unix
        Windows

√ Do you require semicolons? · No / Yes -> Yes

Local ESLint installation not found.
The config that you've selected requires the following dependencies:

eslint@latest

? Would you like to install them now? » No / Yes -> YES

? Which package manager do you want to use? ...
npm

-   [x] yarn
        pnpm

=> Done.

.eslintrc.cjs

```
module.exports = {
    "env": {
        "browser": true,
        "es2021": true
    },
    "extends": "eslint:recommended",
    "overrides": [
        {
            "env": {
                "node": true
            },
            "files": [
                ".eslintrc.{js,cjs}"
            ],
            "parserOptions": {
                "sourceType": "script"
            }
        }
    ],
    "parserOptions": {
        "ecmaVersion": "latest",
        "sourceType": "module"
    },
    "rules": {

    }
};

```
