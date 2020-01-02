# Sassiin CSS

A lightweight sass library.

## Requirements

To use this library you will need a sass preprosessor. You can read more at https://sass-lang.com/install.

You need to have atleast Dart Sass 1.23.0 as this library uses the new `@use` rule that was introduced in that version.

## How to use

Add this `@use` rule to your own scss file.
```scss
@use "sassiin-css";
```
That's it. Make sure that the sassiin directory is in the same folder as your own scss file. If not, alter the `@use` url accordingly.

You can modify many aspects of sassiin, like the number of columns and colors.
```scss
@use "sassiin-css" with (
    $primary-color: tomato
    $base-font-size: 16px
);
```
List of all variables can be found in `_variables.scss`.

Sassiin is also modular. If you don't need some part of sassiin you can leave it out, thus making the final css file smaller.

For example if you only need the sassiin columns and mixins you can do this.

```scss
// variables has to be used if you want to change the default values, otherwise it can be omitted.
@use 'sassiin-css/variables' with (
    $columns: 24
);

@use 'sassiin-css/columns';
@use 'sassiin-css/mixins';
```