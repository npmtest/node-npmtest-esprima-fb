# npmtest-esprima-fb

#### basic test coverage for  [esprima-fb (v15001.1001.0-dev-harmony-fb)](https://github.com/facebook/esprima/tree/fb-harmony)  [![npm package](https://img.shields.io/npm/v/npmtest-esprima-fb.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-esprima-fb) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-esprima-fb.svg)](https://travis-ci.org/npmtest/node-npmtest-esprima-fb)

#### Facebook-specific fork of the esprima project

[![NPM](https://nodei.co/npm/esprima-fb.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/esprima-fb)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-esprima-fb/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-esprima-fb/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-esprima-fb/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-esprima-fb/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-esprima-fb/build/test-report.html)|
| test-server-github : | [![github.com test-server](https://npmtest.github.io/node-npmtest-esprima-fb/GitHub-Mark-32px.png)](https://npmtest.github.io/node-npmtest-esprima-fb/build/app/index.html) | | build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-esprima-fb/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-esprima-fb/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-esprima-fb/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-esprima-fb/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-esprima-fb/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-esprima-fb/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-esprima-fb/build/test-report.html](https://npmtest.github.io/node-npmtest-esprima-fb/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-esprima-fb/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-esprima-fb/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-esprima-fb/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-esprima-fb/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-esprima-fb/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-esprima-fb/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-esprima-fb/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-esprima-fb/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Ariya Hidayat"
    },
    "bin": {
        "esparse": "./bin/esparse.js",
        "esvalidate": "./bin/esvalidate.js"
    },
    "bugs": {
        "url": "http://issues.esprima.org"
    },
    "dependencies": {},
    "description": "Facebook-specific fork of the esprima project",
    "devDependencies": {
        "commander": "~2.5.0",
        "complexity-report": "~1.1.1",
        "escomplex-js": "1.0.0",
        "eslint": "~0.12.0",
        "istanbul": "~0.2.6",
        "jscs": "~1.10.0",
        "json-diff": "~0.3.1",
        "regenerate": "~0.5.4",
        "unicode-6.3.0": "~0.1.0"
    },
    "directories": {},
    "dist": {
        "shasum": "43beb57ec26e8cf237d3dd8b33e42533577f2659",
        "tarball": "https://registry.npmjs.org/esprima-fb/-/esprima-fb-15001.1001.0-dev-harmony-fb.tgz"
    },
    "engines": {
        "node": ">=0.4.0"
    },
    "files": [
        "bin",
        "test/run.js",
        "test/runner.js",
        "test/test.js",
        "test/compat.js",
        "test/reflect.js",
        "esprima.js"
    ],
    "gitHead": "56e06e46f066383a97ce22732f0c9964ef82dc5a",
    "homepage": "https://github.com/facebook/esprima/tree/fb-harmony",
    "licenses": [
        {
            "type": "BSD",
            "url": "http://github.com/facebook/esprima/raw/master/LICENSE.BSD"
        }
    ],
    "main": "esprima.js",
    "maintainers": [
        {
            "name": "jeffmo"
        },
        {
            "name": "zpao"
        },
        {
            "name": "gabelevi"
        }
    ],
    "name": "esprima-fb",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/facebook/esprima.git"
    },
    "scripts": {
        "analyze-coverage": "node node_modules/istanbul/lib/cli.js cover test/runner.js",
        "benchmark": "node test/benchmarks.js",
        "benchmark-quick": "node test/benchmarks.js quick",
        "check-coverage": "node node_modules/istanbul/lib/cli.js check-coverage --statement 100 --branch 100 --function 100",
        "check-version": "node tools/check-version.js",
        "complexity": "node tools/list-complexity.js && cr -s -l -w --maxcyc 18 esprima.js",
        "coverage": "npm run analyze-coverage && npm run check-coverage",
        "eslint": "node node_modules/eslint/bin/eslint.js esprima.js",
        "generate-regex": "node tools/generate-identifier-regex.js",
        "jscs": "jscs esprima.js test/*test.js",
        "lint": "npm run check-version && npm run eslint && npm run jscs && npm run complexity",
        "test": "node test/run.js && npm run lint && npm run coverage"
    },
    "version": "15001.1001.0-dev-harmony-fb"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
