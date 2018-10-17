# VSCode coverage test runner

[![license][license-badge]][LICENSE]

This test runner can be used instead of standard test runner.

## Configuration

Install npm package:

```
npm i -D vscode-coverage-test-runner
```

Replace default test runner in your `test/index.ts` file from `vscode/lib/testrunner` to `vscode-coverage-test-runner`.

```js
var testRunner = require('vscode-coverage-test-runner');
```

Put `coverconfig.json` file into root folder of your project:

```json
{
    "enabled": true,
    "relativeSourcePath": "../src",
    "relativeCoverageDir": "../../coverage",
    "ignorePatterns": [
        "**/node_modules/**"
    ],
    "includePid": false,
    "reports": [
        "html",
        "lcov",
        "text-summary"
    ],
    "verbose": false
}
```

Launch tests!

[LICENSE]: ./LICENSE
[license-badge]: https://img.shields.io/badge/license-MIT-blue.svg
