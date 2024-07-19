# prettier-config

General Intelligence's shared prettier configuration.

## Usage

1. Install the required dependencies in your project:

```
npm i prettier @generalintelligence/prettier-config
```

2. Add a `format` npm run script to your `package.json`:

```
{
  ...
  "scripts": {
    ...
    "format": "prettier --ignore-path ./node_modules/@generalintelligence/prettier-config/.prettierignore . --write"
  }
}
```

3. Install `husky` and add a pre-commit hook to run the formatter:

```
npx husky init
```

Then open `./husky/pre-commit` and add:

```
npm run format
```

That's it. The next time you make a commit, your code should be automatically formatted via this prettier config!

> We also recommend installing the official [Prettier VS Code plugin](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) and enabling the "editor.formatOnSave" setting if you are using VS Code.
