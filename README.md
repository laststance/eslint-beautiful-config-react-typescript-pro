<div align="center">
<h1>eslint-config-ts-prefixer 🌈</h1>

<p>ESLint rule set that integrated <a href="https://prettier.io/">prettier</a> as one of ESLint rule and specialized <a href="https://eslint.org/docs/latest/user-guide/command-line-interface#--fix">fixable</a> rule set :-)</p>
</div>

---

### This config is:
- 📦 Zero extend for [**explicit**](https://github.com/laststance/eslint-config-ts-prefixer/blob/main/index.js) rules.
- 💅 [Prettier](https://prettier.io/) integration, specialized fixable `import` rules.
- ✅ Meamingful rules code behavior.

----

![carbon](https://github.com/laststance/eslint-config-ts-prefixer/assets/5501268/ecd9b954-adf3-48ab-a406-5506070aafd1)


----

# Installation
If you want to manage `.eslintrc.js` file on your codebase, please choose [Barebone Install](#bareborn-install).

## 1. install necessary packages.

```bash
npm install --save-dev eslint-config-ts-prefixer eslint @typescript-eslint/eslint-plugin @typescript-eslint/parser typescript eslint-plugin-import eslint-import-resolver-typescript eslint-plugin-prettier eslint-plugin-sort-keys-fix prettier
```
or using yarn

```bash
yarn add -D eslint-config-ts-prefixer eslint @typescript-eslint/eslint-plugin @typescript-eslint/parser typescript eslint-plugin-import eslint-import-resolver-typescript eslint-plugin-prettier eslint-plugin-sort-keys-fix prettier
```

or using pnpm

```bash
pnpm add -D eslint-config-ts-prefixer eslint @typescript-eslint/eslint-plugin @typescript-eslint/parser typescript eslint-plugin-import eslint-import-resolver-typescript eslint-plugin-prettier eslint-plugin-sort-keys-fix prettier
```


## 2. Setup config files

And then create config files `.eslintrc.js`  `.prettierrc` `.eslintignore` with following command on your project root directory.

```bash
npx eslint-config-ts-prefixer config
```

Now it's ready for use.  
Add script your package.json like this

```json
{
  "scripts": {
    "lint:fix": "eslint src --ext .ts,.tsx,.js,jsx --fix"
  }
}
```

Then you can run via `npm run lint:fix` ESLint & Prettier.  
And if you use VSCode and [ESLint Extension](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint),  
you can get great developer experience with the shortcut.


<div align="left">
  <img src="./assets/extension.png" alt="config"/>
</div>

<br>
<br>

<div align="leftr">
  <p>Perform on Webstorm</p>
    <img src="./assets/autofix.gif" alt="autofix" />
</div>

--------------

Or you can use existing your `.eslintrc.js`, adding "ts-prefixer" in "extends" field manually.  

- ```.eslintrc.js```
```js
{
  extends: ["ts-prefixer"]
}
```

And you need `.prettierrc` file because this package refers your `.prettierrc`.    
If you don't have `.prettierrc`, please `touch .prettierrc` and set prettier rules depends on your preferece like this.

- ```.prettierrc```
```json
{
  "singleQuote": true,
  "semi": false
}
```

--------------

# Bareborn Install
Bareborn Install is creates the eslint-config-ts-prefixer's `.eslintconfig.js` file directly in your code base.  
You can manage the rules yourself.

### 1. install necessary packages.

```bash
npm install --save-dev eslint @typescript-eslint/eslint-plugin @typescript-eslint/parser typescript eslint-plugin-import eslint-import-resolver-typescript eslint-plugin-prettier eslint-plugin-sort-keys-fix prettier
```
or using yarn

```bash
yarn add -D eslint @typescript-eslint/eslint-plugin @typescript-eslint/parser typescript eslint-plugin-import eslint-import-resolver-typescript eslint-plugin-prettier eslint-plugin-sort-keys-fix prettier
```

or using pnpm

```bash
pnpm add -D eslint @typescript-eslint/eslint-plugin @typescript-eslint/parser typescript eslint-plugin-import eslint-import-resolver-typescript eslint-plugin-prettier eslint-plugin-sort-keys-fix prettier
```

### 2. run `npx eslint-config-ts-prefixer barebone`

run  

```bash
npx eslint-config-ts-prefixer barebone
```

And then generated `.eslintrc.js`, `.eslintignore`, `.prettierrc`.

Now it's ready for use.  
Add script your package.json like this

```json
{
  "scripts": {
    "lint:fix": "eslint . --ext .ts,.tsx,.js,jsx --fix"
  }
}
```

Finally run that `npm run lint:fix`


## LICENSE

MIT

