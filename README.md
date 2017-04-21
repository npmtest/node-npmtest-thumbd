# npmtest-thumbd

#### basic test coverage for  thumbd (v2.19.0)  [![npm package](https://img.shields.io/npm/v/npmtest-thumbd.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-thumbd) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-thumbd.svg)](https://travis-ci.org/npmtest/node-npmtest-thumbd)

#### Node.js/AWS/ImageMagick-based image thumbnailing service.

[![NPM](https://nodei.co/npm/thumbd.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/thumbd)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-thumbd/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-thumbd/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-thumbd/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-thumbd/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-thumbd/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-thumbd/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-thumbd/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-thumbd/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-thumbd/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-thumbd/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-thumbd/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-thumbd/build/test-report.html](https://npmtest.github.io/node-npmtest-thumbd/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-thumbd/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-thumbd/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-thumbd/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-thumbd/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-thumbd/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-thumbd/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-thumbd/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-thumbd/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "thumbd",
    "version": "2.19.0",
    "directories": {
        "bin": "./bin",
        "data": "./data",
        "lib": "./lib"
    },
    "main": "./lib/index.js",
    "bin": "./bin/thumbd.js",
    "author": "Ben Coe <bencoe@gmail.com>",
    "engines": {
        "node": "0.10.29"
    },
    "config": {
        "blanket": {
            "data-cover-never": [
                "node_modules",
                "test"
            ],
            "output-reporter": "spec",
            "pattern": "lib"
        }
    },
    "scripts": {
        "coverage": "nyc report --reporter=text-lcov | coveralls",
        "start": "./bin/thumbd.js server",
        "pretest": "standard",
        "test": "nyc mocha"
    },
    "description": "Node.js/AWS/ImageMagick-based image thumbnailing service.",
    "keywords": [
        "image",
        "imagemagick",
        "processing",
        "sqs",
        "thumbnail"
    ],
    "service": {
        "env": {
            "AWS_KEY": {
                "description": "What is your AWS Key (used by SQS and S3)"
            },
            "AWS_REGION": {
                "default": "us-east-1",
                "description": "Default AWS region for SQS and S3."
            },
            "AWS_SECRET": {
                "description": "What is your AWS secret (used by SQS and S3)"
            },
            "BUCKET": {
                "description": "What S3 bucket would you like to store converted thumbnails in"
            },
            "CONVERT_COMMAND": {
                "default": "/usr/local/bin/convert",
                "description": "Absolute path to ImageMagick bin"
            },
            "SQS_QUEUE": {
                "description": "What SQS queue should thumbd fetch work from"
            },
            "TMP_DIR": {
                "default": "/tmp",
                "description": "what folder should thumbd use for temporary files"
            }
        }
    },
    "repository": {
        "type": "git",
        "url": "git://github.com/bcoe/thumbd.git"
    },
    "dependencies": {
        "async": "^0.9.0",
        "aws-sdk": "^2.1.18",
        "knox": "^0.9.2",
        "lodash": "^3.3.1",
        "ndm": "^3.3.1",
        "request": "^2.40.0",
        "sprintf-js": "^1.0.2",
        "tmp": "~0.0.16",
        "yargs": "^3.4.5"
    },
    "devDependencies": {
        "blanket": "^1.1.6",
        "coveralls": "^2.11.3",
        "look": "^0.1.3",
        "mocha": "^2.2.5",
        "nock": "^2.9.1",
        "nyc": "^3.0.1",
        "sinon": "^1.12.2",
        "standard": "^4.5.4"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
