## configure ESLint

using [http://eslint.org/](ESLint) also we use from [https://github.com/airbnb/javascript/tree/master/packages/eslint-config-airbnb](eslint-config-airbnb) Airbnb has great [https://github.com/airbnb/javascript](JavaScript style guide) 

1.add these packages as  dev dependencies

```
yarn add babel-eslint@^7.1.1 eslint@^3.19.0 eslint-config-airbnb@^15.0.1 eslint-config-eslint@^4.0.0 eslint-plugin-import@^2.2.0 eslint-plugin-jsx-a11y@^5.0.3 eslint-plugin-react@^7.1.0 --dev
```

2.add `.eslintrc` config file

```
{
  "extends": [
    "airbnb",
    "eslint",
    "eslint:recommended",
    "plugin:react/recommended"
  ],
  "parser": "babel-eslint",
  "env": {
    "browser": true
  },
  "ecmaFeatures": {
    "classes": true,
    "jsx": true
  },
  "plugins": [
    "react",
    "jsx-a11y",
    "import"
  ],
  "parserOptions": {
    "ecmaVersion": 7,
    "sourceType": "module",
    "ecmaFeatures": {
      "jsx": true
    }
  },
  "rules": {
    "max-len": [
      "error",
      80,
      4,
      {
        "ignoreUrls": true,        
        "ignoreComments": true,
        "ignoreTrailingComments": true,
        "ignoreRegExpLiterals": true
      }
    ],
    "arrow-body-style": "error",
    "arrow-parens": "error",
    "arrow-spacing": "error",
    "eqeqeq": "error",
    "generator-star-spacing": "error",
    "no-duplicate-imports": "error",
    "no-eq-null": "error",
    "no-undefined": "error",
    "no-useless-computed-key": "error",
    "no-useless-constructor": "error",
    "no-useless-rename": "error",
    "no-var": "error",
    "object-shorthand": "error",
    "prefer-arrow-callback": "error",
    "prefer-const": "error",
    "prefer-rest-params": "error",
    "prefer-spread": "error",
    "prefer-template": "error",
    "rest-spread-spacing": "error",
    "semi": "error",
    "template-curly-spacing": "error",
    "yield-star-spacing": "error"
  }
}
```

3.install [https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint](ESLint extension)

4.install [https://marketplace.visualstudio.com/items?itemName=taichi.react-beautify](react-beautify extension)

5.keyboards shortcuts

```
{
  "command": "eslint.executeAutofix",
  "key": "shift+cmd+f"
},
{
  "command": "react.beautify",
  "key": "shift+alt+f"
}
```
