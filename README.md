# testcafe-reporter-xray-vbi
[![Build Status](https://travis-ci.org/s1mob/testcafe-reporter-xray-json.svg)](https://travis-ci.org/s1mob/testcafe-reporter-xray-json)

This is the **xray-vbi** reporter plugin for [TestCafe](http://devexpress.github.io/testcafe).

## Install

```
npm install testcafe-reporter-xray-vbi
```

## Usage

When you run tests from the command line, specify the reporter name by using the `--reporter` option:

```
testcafe chrome 'path/to/test/file.js' --reporter xray-vbi
```


When you use API, pass the reporter name to the `reporter()` method:

```js
testCafe
    .createRunner()
    .src('path/to/test/file.js')
    .browsers('chrome')
    .reporter('xray-vbi') // <-
    .run();
```

## Author
Sivakumar A
