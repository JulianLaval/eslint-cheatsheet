### Best Practices
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
<td>accessor-pairs</td>
<td>Enforces getter/setter pairs in objects</td>
<td>
<pre>
// Good
var o = {
    set a(value) {
        this.val = value;
    },
    get a() {
        return this.val;
    }
};
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/accessor-pairs)</td>
</tr>
<tr>
<td>block-scoped-var</td>
<td>Treat `var` statements as if they were block scoped</td>
<td>
<pre>
function doSomething() {
    if (true) {
        var build = true;
    }
    console.log(build);
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/block-scoped-var)</td>
</tr>
<tr>
<td>complexity</td>
<td>Specify the maximum cyclomatic complexity allowed in a program</td>
<td>
<pre>
// complexity: [1, 2]
function a(x) {
    if (true) {
        return x;
    } else if (false) {
        return x+1;
    } else {
        return 4; // 3rd path
    }
}
</pre>
</td>
<td>Allowed between 0 and 11 levels of complexity</td>
<td>[Link](http://eslint.org/docs/rules/complexity)</td>
</tr>
<tr>
<td>consistent-return</td>
<td>Require `return` statements to either always or never specify values</td>
<td>
<pre>
function doSomething(condition) {
    if (condition) {
        return true;
    } else {
        return;
    }
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/consistent-return)</td>
</tr>
<tr>
<td>curly</td>
<td>Specific curly brace conventions for all control statements</td>
<td>
<pre>
// Bad
if (foo) return;
// Good
if (foo) {
    return;
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/curly)</td>
</tr>
<tr>
<td>default-case</td>
<td>Require `default` case in `switch` statements</td>
<td>
<pre>
switch (foo) {
    case 1:
        doSomething();
        break;
    case 2:
        doSomething();
        break;
    default:
        // do nothing
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/default-case)</td>
</tr>
<tr>
<td>dot-notation</td>
<td>Encourages use of dot notation whenever possible</td>
<td>
<pre>
// Bad
foo["bar"];
// Good
var x = foo.bar;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/dot-notation)</td>
</tr>
<tr>
<td>dot-location</td>
<td>Enforces consistent newlines before or after dots</td>
<td>
<pre>
var a = universe.
        galaxy;

var b = universe
       .galaxy;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/dot-location)</td>
</tr>
<tr>
<td>eqeqeq</td>
<td>Require the use of `===` and `!==`</td>
<td>
<pre>
// Bad
if (x == 42) { ... }
if ("" == text) { ... }
if (obj.getStuff() != undefined) { ... }
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/eqeqeq)</td>
</tr>
<tr>
<td>guard-for-in</td>
<td>Make sure `for-in` loops have an `if` statement</td>
<td>
<pre>
// Bad
for (key in foo) {
    doSomething(key);
}
// Good
for (key in foo) {
    if ({}.hasOwnProperty.call(foo, key)) {
        doSomething(key);
    }
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/guard-for-in)</td>
</tr>
<tr>
<td>no-alert</td>
<td>Disallow the use of `alert`, `confirm`, and `prompt`</td>
<td>
<pre>
// Bad
alert("here!");
confirm("Are you sure?");
prompt("What's your name?", "John Doe");
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-alert)</td>
</tr>
<tr>
<td>no-caller</td>
<td>Disallow the use of `arguments.caller` or `arguments.callee`</td>
<td>
<pre>
function foo() {
    var callee = arguments.callee;
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-caller)</td>
</tr>
<tr>
<td>no-div-regex</td>
<td>Disallow division operators explicitly at beginning of regular expression</td>
<td>
<pre>
// Bad
function() { return /=foo/; }
// Good
function() { return /\=foo/; }
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-div-regex)</td>
</tr>
<tr>
<td>no-else-return</td>
<td>Disallow `else` after a `return` in an `if`</td>
<td>
<pre>
function foo() {
    if (x) {
        return y;
    } else {
        return z;
    }
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-else-return)</td>
</tr>
<tr>
<td>no-empty-label</td>
<td>Disallow use of labels for anything other than loops and switches</td>
<td>
<pre>
labeled: //Label for the following var statement
    var x = 10;
};
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-empty-label)</td>
</tr>
<tr>
<td>no-eq-null</td>
<td>Disallow comparisons to null without a type-checking operator</td>
<td>
<pre>
if (foo == null) {
  bar();
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-eq-null)</td>
</tr>
<tr>
<td>no-eval</td>
<td>Disallow use of `eval()`</td>
<td>
<pre>
// Bad
var obj = { x: "foo" },
    key = "x",
    value = eval("obj." + key);
// Good
var obj = { x: "foo" },
    key = "x",
    value = obj[key];
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-eval)</td>
</tr>
<tr>
<td>no-extend-native</td>
<td>Disallow adding to native types</td>
<td>
<pre>
// seems harmless
Object.prototype.extra = 55;

// loop through some userIds
var users = {
    "123": "Stan",
    "456": "David"
};

// not what you'd expect
for (var id in users) {
    console.log(id); // "123", "456", "extra"
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-extend-native)</td>
</tr>
<tr>
<td>no-extra-bind</td>
<td>Disallow unnecessary function binding</td>
<td>
<pre>
var foo = function() { // function doesn't use this
  do(stuff);
}.bind(bar)
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-extra-bind)</td>
</tr>
<tr>
<td>no-fallthrough</td>
<td>Disallow fallthrough of `case` statements</td>
<td>
<pre>
// Bad
switch(foo) {
    case 1:
        doSomething();
    case 2:
        doSomethingElse();
}
// Good
switch(foo) {
    case 1:
        doSomething();
        break;
    case 2:
        doSomethingElse();
}
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-fallthrough)</td>
</tr>
<tr>
<td>no-floating-decimal</td>
<td>Disallow the use of leading or trailing decimal points in numeric literals</td>
<td>
<pre>
var num = .5;
var num = 2.;
var num = -.7;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-floating-decimal)</td>
</tr>
<tr>
<td>no-implicit-coercion</td>
<td>Disallow the type conversions with shorter notations</td>
<td>
<pre>
// Bad
var b = !!foo;
var n = 1 * foo;
var s = "" + foo;
// Good
var b = Boolean(foo);
var n = Number(foo);
var s = String(foo);
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-implicit-coercion)</td>
</tr>
<tr>
<td>no-implied-eval</td>
<td>Disallow use of `eval()`-like methods</td>
<td>
<pre>
setTimeout("alert('Hi!');", 100);
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-implied-eval)</td>
</tr>
<tr>
<td>no-invalid-this</td>
<td>Disallow `this` keywords outside of classes or class-like objects</td>
<td>
<pre>
this.a = 0;
baz(() => this);
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-invalid-this)</td>
</tr>
<tr>
<td>no-iterator</td>
<td>Disallow usage of `__iterator__` property</td>
<td>
<pre>
Foo.prototype.__iterator__ = function() {
    return new FooIterator(this);
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-iterator)</td>
</tr>
<tr>
<td>no-labels</td>
<td>Disallow use of labeled statements</td>
<td>
<pre>
outer:
    while (true) {
        while (true) {
            break outer;
        }
    }
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-labels)</td>
</tr>
<tr>
<td>no-lone-blocks</td>
<td>Disallow unnecessary nested blocks</td>
<td>
<pre>
{
    var foo = bar();
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-lone-blocks)</td>
</tr>
<tr>
<td>no-loop-func</td>
<td>Disallow creation of functions within loops</td>
<td>
<pre>
for (var i = 0; i < 10; i++) {
    funcs[i] = function() {
        return i;
    };
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-loop-func)</td>
</tr>
<tr>
<td>no-multi-spaces</td>
<td>Disallow use of multiple spaces</td>
<td>
<pre>
if(foo     === "bar") {}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-multi-spaces)</td>
</tr>
<tr>
<td>no-multi-str</td>
<td>Disallow use of multiline strings</td>
<td>
<pre>
var x = "Line 1 \
         Line 2";
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-multi-str)</td>
</tr>
<tr>
<td>no-native-reassign</td>
<td>Disallow reassignments of native objects</td>
<td>
<pre>
String = "hello world";
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-native-reassign)</td>
</tr>
<tr>
<td>no-new-func</td>
<td>Disallow use of new operator for `Function` object</td>
<td>
<pre>
var x = new Function("a", "b", "return a + b");
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-new-func)</td>
</tr>
<tr>
<td>no-new-wrappers</td>
<td>Disallows creating new instances of `String`, `Number`, and `Boolean`</td>
<td>
<pre>
var stringObject = new String("Hello world");
var numberObject = new Number(33);
var booleanObject = new Boolean(false);
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-new-wrappers)</td>
</tr>
<tr>
<td>no-new</td>
<td>Disallow use of the `new` operator when not part of an assignment or comparison</td>
<td>
<pre>
// Bad
new Person();
// Good
var person = new Person();
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-new)</td>
</tr>
<tr>
<td>no-octal-escape</td>
<td>Disallow use of octal escape sequences in string literals</td>
<td>
<pre>
var foo = "Copyright \251";
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-octal-escape)</td>
</tr>
<tr>
<td>no-octal</td>
<td>Disallow use of octal literals</td>
<td>
<pre>
var num = 071;      // 57
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-octal)</td>
</tr>
<tr>
<td>no-param-reassign</td>
<td>Disallow reassignment of function parameters</td>
<td>
<pre>
function foo(bar) {
    bar = 13;
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-param-reassign)</td>
</tr>
<tr>
<td>no-process-env</td>
<td>Disallow use of `process.env`</td>
<td>
<pre>
if(process.env.NODE_ENV === "development") {
    //...
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-process-env)</td>
</tr>
<tr>
<td>no-proto</td>
<td>Disallow usage of `__proto__` property</td>
<td>
<pre>
// Bad
var a = obj.__proto__;
// Good
var a = Object.getPrototypeOf(obj);
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-proto)</td>
</tr>
<tr>
<td>no-redeclare</td>
<td>Disallow declaring the same variable more than once</td>
<td>
<pre>
var a = 3;
var a = 10; // redeclared
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-redeclare)</td>
</tr>
<tr>
<td>no-return-assign</td>
<td>Disallow use of assignment in `return` statement</td>
<td>
<pre>
function doSomething() {
    return foo = bar + 2;
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-return-assign)</td>
</tr>
<tr>
<td>no-script-url</td>
<td>Disallow use of `javascript:` urls</td>
<td>
<pre>
location.href = "javascript:void(0)";
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-script-url)</td>
</tr>
<tr>
<td>no-self-compare</td>
<td>Disallow comparisons where both sides are exactly the same</td>
<td>
<pre>
var x = 10;
if (x === x) {
    x = 20;
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-self-compare)</td>
</tr>
<tr>
<td>no-sequences</td>
<td>Disallow use of the comma operator</td>
<td>
<pre>
var a = (3, 5); // a = 5
a = b += 5, a + b;
while (a = next(), a && a.length);
(0,eval)("doSomething();");
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-sequences)</td>
</tr>
<tr>
<td>no-throw-literal</td>
<td>Restrict what can be thrown as an exception</td>
<td>
<pre>
// Bad
throw "error";
throw 0;
throw undefined;
throw null;
// Good
throw new Error();
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-throw-literal)</td>
</tr>
<tr>
<td>no-unused-expressions</td>
<td>Disallow usage of expressions in statement position</td>
<td>
<pre>
"Hello world";
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-unused-expressions)</td>
</tr>
<tr>
<td>no-useless-call</td>
<td>Disallow unnecessary `.call()` and `.apply()`</td>
<td>
<pre>
// Those are same as `foo(1, 2, 3);`
foo.call(undefined, 1, 2, 3);
foo.apply(undefined, [1, 2, 3]);
foo.call(null, 1, 2, 3);
foo.apply(null, [1, 2, 3]);
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-useless-call)</td>
</tr>
<tr>
<td>no-void</td>
<td>Disallow use of the `void` operator</td>
<td>
<pre>
// will always return undefined
(function(){
    return void 0;
})();
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-void)</td>
</tr>
<tr>
<td>no-warning-comments</td>
<td>Disallow usage of configurable warning terms in comments</td>
<td>
<pre>
// with "TODO" set as warning term

// TODO: this
// todo: this too
// Even this: TODO
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-warning-comments)</td>
</tr>
<tr>
<td>no-with</td>
<td>Disallow use of the `with` statement</td>
<td>
<pre>
with (foo) {
    // ...
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-with)</td>
</tr>
<tr>
<td>radix</td>
<td>Require use of the second argument for `parseInt()`</td>
<td>
<pre>
// Bad
var num = parseInt("071");      // 57
// Good
var num = parseInt("071", 10);  // 71
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/radix)</td>
</tr>
<tr>
<td>vars-on-top</td>
<td>Require declarations of all vars at the top of their containing scope</td>
<td>
<pre>
function doSomething() {
    var first;
    if (true) {
        first = true;
    }
    var second; //not declared at the top
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/vars-on-top)</td>
</tr>
<tr>
<td>wrap-iife</td>
<td>Require immediate function invocation to be wrapped in parentheses</td>
<td>
<pre>
// Bad
var x = function () { return { y: 1 };}();
// Good
var x = (function () { return { y: 1 };})();
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/wrap-iife)</td>
</tr>
<tr>
<td>yoda</td>
<td>Require or disallow Yoda conditions</td>
<td>
<pre>
if ("red" === color) {
    // ...
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/yoda)</td>
</tr>
</tbody>
<table>
