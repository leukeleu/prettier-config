# Leukeleu Prettier configuration

## Installing this package

If you already had Prettier installed in your project you can delete this first with `npm uninstall prettier`.

Then install this package as a development dependency `npm i -D @leukeleu/prettier-config`.

## Adding the config

In your `.prettierrc.js` add:

```js
module.exports = require('@leukeleu/prettier-config')
```

## Add script commands to package.json

To run Prettier on your code, add the following script to your package.json:

```js
"scripts": {
  "prettier": "prettier . --cache",
  "lint:prettier": "npm run prettier -- --check",
  "lintfix:prettier": "npm run prettier -- --write",
}
```

## Running the check

Now you can run the Prettier check using `npm run lint:prettier` or `npm run lintfix:prettier` to auto fix.

## Extending/ changing config

This is not recommended as the goal is have similar settings in all projects, but if for some reason you need to add or change the config it's possible. The config is in JavaScript, so you can make use of the spread operator to extend the config.

```js
module.exports = {
  ...require('@leukeleu/prettier-config'),
  semi: true,
}
```

## Contributing

To learn how to local test and publish this package, please refer to the instructions in the `CONTRIBUTORS.md` file.
