### Variables
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
<td>init-declarations</td>
<td>Enforce or disallow variable initializations at definition</td>
<td>
<pre>
var foo = 1;
var bar;

bar = 2;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/init-declarations)</td>
</tr>
<tr>
<td>no-catch-shadow</td>
<td>Disallow the catch clause parameter name being the same as a variable in the outer scope</td>
<td>
<pre>
var err = "x";
try {
    throw "problem";
} catch (err) {}
console.log(err)    // err is 'problem', not 'x'
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-catch-shadow)</td>
</tr>
<tr>
<td>no-delete-var</td>
<td>Disallow deletion of variables</td>
<td>
<pre>
var x;
delete x;
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-delete-var)</td>
</tr>
<tr>
<td>no-label-var</td>
<td>Disallow labels that share a name with a variable</td>
<td>
<pre>
var x = foo;
function bar() {
x:
  for (;;) {
    break x;
  }
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-label-var)</td>
</tr>
<tr>
<td>no-shadow-restricted-names</td>
<td>Disallow shadowing of names such as `arguments`</td>
<td>
<pre>
var undefined = "foo";
!function(Infinity){};
function NaN(){}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-shadow-restricted-names)</td>
</tr>
<tr>
<td>no-shadow</td>
<td>Disallow declaration of variables already declared in the outer scope</td>
<td>
<pre>
var a = 3;
function b() {
    var a = 10;
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-shadow)</td>
</tr>
<tr>
<td>no-undef-init</td>
<td>Disallow use of undefined when initializing variables</td>
<td>
<pre>
// Bad
var foo = undefined;
// Good
var foo;
console.log(foo === undefined);     // true
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-undef-init)</td>
</tr>
<tr>
<td>no-undef</td>
<td>Disallow use of undeclared variables unless mentioned in a `/*global */` block</td>
<td>
<pre>
var a = someFunction();  // 'someFunction' is not defined.
b = 10;                  // 'b' is not defined.
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-undef)</td>
</tr>
<tr>
<td>no-undefined</td>
<td>Disallow use of `undefined` variable</td>
<td>
<pre>
var undefined = "hi";
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-undefined)</td>
</tr>
<tr>
<td>no-unused-vars</td>
<td>Disallow declaration of variables that are not used in the code</td>
<td>
<pre>
var y = 10;
y = 5;
// By default, unused arguments cause warnings.
(function(foo) {
    return 5;
})();
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-unused-vars)</td>
</tr>
<tr>
<td>no-use-before-define</td>
<td>Disallow use of variables before they are defined</td>
<td>
<pre>
alert(a);
var a = 10;

f();
function f() {}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-use-before-define)</td>
</tr>
</tbody>
<table>
