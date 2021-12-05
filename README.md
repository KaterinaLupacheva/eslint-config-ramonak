# Eslint, TypeScript, and Prettier Setup

These are my Eslint, TypeScript, and Prettier settings that I use in React.js projects.

## Usage

1.Install peer dependencies:

```bash
npx install-peerdeps --dev eslint-config-ramonak
```

2.Tell your project to use eslint-config-ramonak. For that,

- in `package.json` add or edit (if already exists) `eslintConfig` field:

```json
"eslintConfig": {
    "extends": [
      "ramonak"
    ]
  }
```

- OR create `.eslintrc` file with the following content:

```json
{
  "extends": ["ramonak"]
}
```

3.To lint your code run:

```bash
npx eslint .
```

OR if you'd like fixable errors to be fixed automatically, run:

```bash
npx eslint . --fix
```

**NOTE:** This config works only for TypeScript projects, e.g., your project must include `.tsconfig.json` file. If it doesn't, you can easily initialize it by running:

```bash
npx tsc --init
```

## Override default config

Add your custom ESLint or Prettier rules directly in `.eslintrc` or `package.json` file under `"rules"` (for ESLint) or `"prettier/prettier"` (for Prettier) field:

```json
{
  "extends": ["ramonak"],
  "rules": {
    "@typescript-eslint/ban-ts-comment": "off",
    "prettier/prettier": [
      "error",
      {
        "endOfLine": "auto"
      }
    ]
  }
}
```
