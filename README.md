# Node package self-ref test

Node modules are allowed to import the package they belong to by name. This repo exists to test the intricacies of that behavior. Here is what I have observed:

## Nested packages

When nested packages are present, a self-reference can only be made to the nearest containing package.

```sh
node bar/test-bar.js // logs bar
node bar/test-foo.js // errors
```