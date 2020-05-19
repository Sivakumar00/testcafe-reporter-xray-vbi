# testcafe-reporter-xray-vbi

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

Add the following metadata:

```
fixture `Login Test`
  .meta({
    testPlanKey:'TX-305',                     // ** Compulsory ** //
    summary : "Summary",                      // ** Compulsory ** //
    description : "Description",              // ** Compulsory ** //
    testExecutionKey: 'TX-515',               // ** Needs when you update the execution ** //  
    testEnvironments:['QA']                     // ** Compulsory ** //
  })
  
test('should log into app.powerbi.com', async t => {
  await t
    .useRole(validUser)
    .takeScreenshot('test-1.png')
    .expect(homePage.siteTitle.exists).ok();
    console.log('Verified Home page')
    console.log(t.getBrowserConsoleMessages())
    
}).meta({testKey:'TX-148'});
```

## Author
Sivakumar A
