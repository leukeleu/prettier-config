# Frontend checks

## Installing this package

If you already had Prettier installed in your project you can delete this first with `npm uninstall prettier`.

Then install this package as a development dependency `npm i -D @leukeleu/prettier-config`.

## Adding the config

In your `prettier.config.js` add:

```js
module.exports = require('@leukeleu/prettier-config')
```

## Running the check

You can just use the normal Prettier cli to run the check e.g. `prettier --check .`

## Extending/ changing config

This is not recommended as the goal is have similar settings in all projects, but if for some reason you need to add or change the config it's possible. The config is in JavaScript, so you can make use of the spread operator to extend the config.

```js
module.exports = {
  ...require('@leukeleu/prettier-config'),
  semi: true,
}
```

## Testing this package

To reduce the chances of publishing bugs, test your package before publishing it to the npm registry. Run npm install with the full path to your package directory. You can get this path with `pwd` in your terminal.

`npm install <local path to this repo>`
