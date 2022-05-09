<p align="center">
  <img src="https://github.com/vinccool96/nuxt-storm-old/blob/master/nuxt-webstorm.png?raw=true" />
  <img src="https://github.com/vinccool96/nuxt-storm-old/blob/master/nuxt-phpstorm.png?raw=true" />
</p>

# nuxt-storm-old

[![npm version][npm-version-src]][npm-version-href]
[![License][license-src]][license-href]
<!-- [![npm downloads][npm-downloads-src]][npm-downloads-href] -->

> [NuxtJS](https://nuxtjs.org) module for [WebStorm](https://jetbrains.com/webstorm/)
> and [PhpStorm](https://jetbrains.com/phpstorm/)  that assists with
> using [@nuxt/components](https://github.com/nuxt/components)

## Quick Setup

1. Add `nuxt-storm` to your project as a development dependency

```sh
# Using yarn
yarn add --dev nuxt-storm-old
# Using npm
npm install --save-dev nuxt-storm-old
```

2. Add `.components.gen.js` to your `.gitignore` file

3. Add 'nuxt-storm' to the `buildModules` section of `nuxt.config.js`

```js
{
  buildModules: [
    'nuxt-storm',
  ]
}
```

ℹ️ If you are using `nuxt < 2.9.0`, use `modules` property instead.

That's it! Restart your `yarn dev` and components should now be found ✨

### Nested Components Support

Add `nested: true` in your buildModule inclusion

```js
{
  buildModules: [
    ['nuxt-storm', { nested: true }],
  ]
}
```

If you have components in nested directories:

```bash
| components/
---| My/
------| Form/
---------| TextArea.vue
```

The component name will contain its path:

```html

<MyFormTextArea/>
```

### Path alias

Should your IDE fail to recognize vue component by its absolute path, you can replace it with path alias (default '@').

Thus, the aforementioned component path will be listed as
`@/components/My/Form/TextArea.vue`
instead of
`C:/some/absolute/path/project/components/My/Form/TextArea.vue`.

Add `alias: true` in your buildModule inclusion or set a custom alias as its value should you use one.

```js
{
  buildModules: [
    ['nuxt-storm', {alias: true}],
  ]
}
```

### 🙏 Thanks

This was made possible by with the help of [grunghi](https://github.com/grunghi) and [eggsy](https://github.com/eggsy/)


<!-- Badges -->

[npm-version-src]: https://img.shields.io/npm/v/nuxt-storm-old/latest.svg

[npm-version-href]: https://npmjs.com/package/nuxt-storm-old

[npm-downloads-src]: https://img.shields.io/npm/dt/nuxt-storm-old.svg

[npm-downloads-href]: https://npmjs.com/package/nuxt-storm-old

[license-src]: https://img.shields.io/npm/l/nuxt-storm-old.svg

[license-href]: https://npmjs.com/package/nuxt-storm-old
