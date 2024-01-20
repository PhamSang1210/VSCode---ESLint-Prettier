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
npm i -D eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-config-airbnb-base eslint-plugin-node eslint-config-node
```
or
```
yarn add --dev eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-config-airbnb-base eslint-plugin-node eslint-config-node
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

<h4 id="four">4. Create .eslintrc.json file (You can generate with npx eslint --init)</h4>

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
<h4 id="four">5.Package npm init @eslint/config</h4>
```
npm install @eslint/config
```
