# SassyCast

SassyCast is a simple API for type conversion in Sass.

## Installation

This has been forked from [KittyGiraudel/SassyCast](https://github.com/KittyGiraudel/SassyCast) to remove the `test` and `build` scripts, and to remove the `devDependencies`. This is to remove the need to install [`node-gyp`](https://github.com/nodejs/node-gyp) and its related complications when installing via npm. Note that the original package is abandoned and this fork is primarily for backward compatibility with some projects so is unlikely to receive any new features. To install via npm:

```
npm install github:Ambient-Impact/SassyCast#main --save-dev
```

Original install instructions:

```
gem install SassyCast
```

```
bower install sassy-cast
```

## Notes

SassCast has a strict mode in which it will throw errors when failing to cast values (most notably to colors and numbers). You can enable strict-mode with:

```scss
$sc-strict-mode: true;
```

In non-strict mode, when a value cannot be converted to a number, SassyCast will warn and return `0`. You can change this value with:

```scss
$sc-non-strict-default-number: 0;
```

In non-strict mode, when a value cannot be converted to a color, SassyCast will warn and return `transparent`. You can change this value with:

```scss
$sc-non-strict-default-color: transparent;
```

Note that color formats are sometimes converted automatically by Sass depending on the type of syntaxe used (compressed, expanded, etc.). When casting a color to string, the resulting string can be different from the color input.

## Credits

Huge thanks to [Marc Mintel](http://twitter.com/marcmintel) for his help.
