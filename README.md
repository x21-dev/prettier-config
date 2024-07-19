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

3. Install `husky` and add a pre-commit hook to run the formatter:

```
npx husky init
```

Then open `./husky/pre-commit` and add:

```
npm run format
```
