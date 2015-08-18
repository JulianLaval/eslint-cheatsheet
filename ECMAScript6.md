### ECMAScript 6
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
<td>arrow-parens</td>
<td>Require parens in arrow function arguments</td>
<td>
<pre>
// Bad
a => {}
// Good
(a) => {}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/arrow-parens)</td>
</tr>
<tr>
<td>arrow-spacing</td>
<td>Require space before/after arrow function's arrow</td>
<td>
<pre>
// { "before": true, "after": true }
(a) => {}
// { "before": false, "after": false }
(a)=>{}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/arrow-spacing)</td>
</tr>
<tr>
<td>constructor-super</td>
<td>Verify calls of `super()` in constructors</td>
<td>
<pre>
class A {
    constructor() {
        super(); // unexpected `super()`.
    }
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/constructor-super)</td>
</tr>
<tr>
<td>generator-star-spacing</td>
<td>Enforce spacing around the `*` in generator functions</td>
<td>
<pre>
function* generator() {}
function *generator() {}
function * generator() {}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/generator-star-spacing)</td>
</tr>
<tr>
<td>no-class-assign</td>
<td>Disallow modifying variables of class declarations</td>
<td>
<pre>
class A { }
A = 0;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-class-assign)</td>
</tr>
<tr>
<td>no-const-assign</td>
<td>Disallow modifying variables that are declared using `const`</td>
<td>
<pre>
const a = 0;
a = 1;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-const-assign)</td>
</tr>
<tr>
<td>no-this-before-super</td>
<td>Disallow use of `this`/`super` before calling `super()` in constructors</td>
<td>
<pre>
class A extends B {
    constructor() {
        this.a = 0; // this is before `super()`.
        super();
    }
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-this-before-super)</td>
</tr>
<tr>
<td>no-var</td>
<td>Require `let` or `const` instead of `var`</td>
<td>
<pre>
var x = "y";
var CONFIG = {};

let x = "y";
const CONFIG = {};
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-var)</td>
</tr>
<tr>
<td>object-shorthand</td>
<td>Require method and property shorthand syntax for object literals</td>
<td>
<pre>
var foo = {
    a: function() {},
    b: function() {}
};

var foo = {
    a() {},
    b() {}
};
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/object-shorthand)</td>
</tr>
<tr>
<td>prefer-const</td>
<td>Suggest using `const` declaration for variables that are never modified after declared</td>
<td>
<pre>
for (let i in [1,2,3]) { // `i` is re-defined (not modified) on each loop step.
    console.log(i);
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/prefer-const)</td>
</tr>
<tr>
<td>prefer-spread</td>
<td>Suggest using the spread operator instead of `.apply()`</td>
<td>
<pre>
var args = [1, 2, 3, 4];
Math.max.apply(Math, args);

var args = [1, 2, 3, 4];
Math.max(...args);
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/prefer-spread)</td>
</tr>
<tr>
<td>prefer-reflect</td>
<td>Suggest using Reflect methods where applicable</td>
<td>
<pre>
foo.apply(undefined, args);
obj.foo.apply(obj, args);

foo.call(undefined, arg);
obj.foo.call(obj, arg);
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/prefer-reflect)</td>
</tr>
<tr>
<td>require-yield</td>
<td>Disallow generator functions that do not have `yield`</td>
<td>
<pre>
function* foo() {
  yield 5;
  return 10;
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/require-yield)</td>
</tr>
</tbody>
<table>
