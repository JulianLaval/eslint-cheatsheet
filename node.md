### Node.js
<table>
<thead>
<tr>
<th>Rule</th>
<th>Description</th>
<th>Snippet</th>
<th>ESLint Default</th>
<th>Link</th>
</tr>
</thead>
<tbody>
<tr>
<td>callback-return</td>
<td>Enfore `return` after a callback</td>
<td>
<pre>
// Good
function foo() {
    if (err) {
        return callback(err);
    }
    callback();
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/callback-return)</td>
</tr>
<tr>
<td>handle-callback-err</td>
<td>Enfore error handling in callbacks</td>
<td>
<pre>
function loadData (err, data) {
    doSomething(); // forgot to handle error
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/handle-callback-err)</td>
</tr>
<tr>
<td>no-mixed-requires</td>
<td>Disallow mixing regular variable and require declarations</td>
<td>
<pre>
var fs = require('fs'),        // "core" 
    async = require('async'),  // "module" 
    baz = 42,                  // "other"
    bam;                       // "uninitialized"
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-mixed-requires)</td>
</tr>
<tr>
<td>no-new-require</td>
<td>Disallow use of `new` operator with the `require` function</td>
<td>
<pre>
// Bad
var appHeader = new require('app-header');
// Good
var AppHeader = require('app-header');
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-new-require)</td>
</tr>
<tr>
<td>no-path-concat</td>
<td>Disallow string concatenation with `__dirname` and `__filename`</td>
<td>
<pre>
// Bad
var fullPath = __dirname + "/foo.js";
// Good
var fullPath = path.join(__dirname, "foo.js");
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-path-concat)</td>
</tr>
<tr>
<td>no-process-exit</td>
<td>Disallow `process.exit()`</td>
<td>
<pre>
// Bad
if (somethingBadHappened) {
    console.error("Something bad happened!");
    process.exit(1);
}
// Good
if (somethingBadHappened) {
    throw new Error("Something bad happened!");
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-process-exit)</td>
</tr>
<tr>
<td>no-restricted-modules</td>
<td>Restrict usage of specified node modules</td>
<td>
<pre>
// With "fs" restricted
var fs = require('fs'); // Disallowed
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-restricted-modules)</td>
</tr>
<tr>
<td>no-sync</td>
<td>Disallow use of synchronous methods</td>
<td>
<pre>
fs.existsSync(somePath);
var contents = fs.readFileSync(somePath).toString();
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-sync)</td>
</tr>
</tbody>
<table>
