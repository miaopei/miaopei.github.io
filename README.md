# Hexo Blog

fix:

(node:38910) [DEP0040] DeprecationWarning: The `punycode` module is deprecated. Please use a userland alternative instead.
(Use `node --trace-deprecation ...` to show where the warning was created)

```shell
vi node_modules/tr46/index.js
// Replace this:
const punycode = require('punycode');
// With this:
const punycode = require('punycode/');
```

