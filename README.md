Behavior prior to commit 39d8fc8ebb7b1354d5f723c8f9bff62f292d19a6

```
c:\code\import-pulumi>pulumi preview
Previewing update (dev)

View Live: <redacted>

     Type                 Name               Plan
     pulumi:pulumi:Stack  import-pulumi-dev

Resources:
    1 unchanged
```

Behavior after commit 39d8fc8ebb7b1354d5f723c8f9bff62f292d19a6

```
c:\code\import-pulumi>pulumi preview
Previewing update (dev)

View Live: <redacted>

     Type                 Name               Plan     Info
     pulumi:pulumi:Stack  import-pulumi-dev           1 error

Diagnostics:
  pulumi:pulumi:Stack (import-pulumi-dev):
    error: Running program 'c:\code\import-pulumi' failed with an unhandled exception:
    Error [ERR_REQUIRE_ESM]: require() of ES Module c:\code\import-pulumi\index.js from c:\code\import-pulumi\node_modules\@pulumi\pulumi\cmd\run\run.js not supported.
    Instead change the require of index.js in c:\code\import-pulumi\node_modules\@pulumi\pulumi\cmd\run\run.js to a dynamic import() which is available in all CommonJS modules.
        at Object.<anonymous> (c:\code\import-pulumi\node_modules\@pulumi\pulumi\cmd\run\run.js:219:31)
        at Generator.next (<anonymous>)
        at c:\code\import-pulumi\node_modules\@pulumi\pulumi\cmd\run\run.js:21:71
        at new Promise (<anonymous>)
        at __awaiter (c:\code\import-pulumi\node_modules\@pulumi\pulumi\cmd\run\run.js:17:12)
        at Object.runProgram [as init] (c:\code\import-pulumi\node_modules\@pulumi\pulumi\cmd\run\run.js:205:30)
        at Stack.<anonymous> (c:\code\import-pulumi\node_modules\@pulumi\pulumi\runtime\stack.js:86:43)
        at Generator.next (<anonymous>)
        at fulfilled (c:\code\import-pulumi\node_modules\@pulumi\pulumi\runtime\stack.js:18:58)

```
