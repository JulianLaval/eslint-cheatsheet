### All Enabled Rules
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
<td>comma-dangle</td>
<td>Disallow or enforce trailing commas</td>
<td>
<pre>
 var foo = {
    bar: "baz",
    qux: "quux",
}; 
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/comma-dangle)</td>
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
<td>no-cond-assign</td>
<td>Disallow assignment in conditional expressions</td>
<td>
<pre>
// Check the user's job title
if (user.jobTitle = "manager") {
    // user.jobTitle is now incorrect
}
</pre>
</td>
<td>Error except enclosed in extra parentheses</td>
<td>[Link](http://eslint.org/docs/rules/no-cond-assign)</td>
</tr>
<tr>
<td>no-console</td>
<td>Disallow use of console in the node environment</td>
<td>
<pre>
console.log("Made it here.");
console.error("That shouldn't have happened.");
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-console)</td>
</tr>
<tr>
<td>no-constant-condition</td>
<td>Disallow use of constant expressions in conditions</td>
<td>
<pre>
if (false) {
    doSomethingUnfinished();
}
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-constant-condition)</td>
</tr>
<tr>
<td>no-control-regex</td>
<td>Disallow control characters in regular expressions</td>
<td>
<pre>
var pattern1 = /\\x1f/;
var pattern2 = new RegExp("\x1f");
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-control-regex)</td>
</tr>
<tr>
<td>no-debugger</td>
<td>Disallow use of debugger</td>
<td>
<pre>
debugger;
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-debugger)</td>
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
<td>no-dupe-args</td>
<td>Disallow duplicate arguments in functions</td>
<td>
<pre>
function (a, b, a) {
    console.log("which a is it?", a);
}
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-dupe-args)</td>
</tr>
<tr>
<td>no-dupe-keys</td>
<td>Disallow duplicate keys when creation object literals</td>
<td>
<pre>
var foo = {
    bar: "baz",
    bar: "qux"
};
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-dupe-keys)</td>
</tr>
<tr>
<td>no-duplicate-case</td>
<td>Disallow a duplicate case label</td>
<td>
<pre>
var a = 1;

switch (a) {
    case 1:
        break;
    case 2:
        break;
    case 1:         // duplicate literal 1
        break;
    default:
        break;
}
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-duplicate-case)</td>
</tr>
<tr>
<td>no-empty</td>
<td>Disallow empty statements</td>
<td>
<pre>
if (foo) {
}
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-empty)</td>
</tr>
<tr>
<td>no-empty-character-class</td>
<td>Disallow the use of empty character classes in regular expressions</td>
<td>
<pre>
var foo = /^abc[]/;
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-empty-character-class)</td>
</tr>
<tr>
<td>no-ex-assign</td>
<td>Disallow assigning to the exception in a catch block</td>
<td>
<pre>
try {
    // code
} catch (e) {
    e = 10;
}
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-ex-assign)</td>
</tr>
<tr>
<td>no-extra-boolean-cast</td>
<td>Disallow double-negation boolean casts in a boolean context</td>
<td>
<pre>
if (!!foo) {
    // ...
}
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-extra-boolean-cast)</td>
</tr>
<tr>
<td>no-extra-semi</td>
<td>Disallow unnecessary semicolons</td>
<td>
<pre>
var x = 5;;
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-extra-semi)</td>
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
<td>no-func-assign</td>
<td>Disallow overwriting functions written as function declarations</td>
<td>
<pre>
function foo() {}
foo = bar;
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-func-assign)</td>
</tr>
<tr>
<td>no-inner-declarations</td>
<td>Disallow function or variable declarations in nested blocks</td>
<td>
<pre>
if (test) {
    function doSomethingElse () { }
}

function anotherThing() {
    var fn;
    if (test) {
        // Good
        fn = function expression() { };
        // Bad
        function declaration() { }
    }
}
</pre>
</td>
<td>Error in functions</td>
<td>[Link](http://eslint.org/docs/rules/no-inner-declarations)</td>
</tr>
<tr>
<td>no-invalid-regexp</td>
<td>Disallow invalid regular expression strings in the RegExp constructor</td>
<td>
<pre>
RegExp('['])
RegExp('.', 'z') // invalid flags
new RegExp('\\')
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-invalid-regexp)</td>
</tr>
<tr>
<td>no-irregular-whitespace</td>
<td>Disallow irregular whitespace outside of strings and comments</td>
<td>
<pre>
function thing()<NBSP>{  return 'test'; }
function thing(<NBSP>){  return 'test'; }
function thing<NBSP>(){  return 'test'; }
function thing<MVS>(){  return 'test'; }
function thing() {  return 'test';<ZWSP> }
function thing() {  return 'test';<NBSP> }
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-irregular-whitespace)</td>
</tr>
<tr>
<td>no-mixed-spaces-and-tabs</td>
<td>Disallow mixed spaces and tabs for indentation</td>
<td>
<pre>
function main() {
--->var x = 5,
--->....y = 7;
}
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-mixed-spaces-and-tabs)</td>
</tr>
<tr>
<td>no-negated-in-lhs</td>
<td>Disallow negation of the left operand of an in expression</td>
<td>
<pre>
// Bad
if(!a in b) // do something
// Good
if(('' + !a) in b) // do something
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-negated-in-lhs)</td>
</tr>
<tr>
<td>no-obj-calls</td>
<td>Disallow the use of object properties of the global object (Math and JSON) as functions</td>
<td>
<pre>
var x = Math();
var y = JSON();
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-obj-calls)</td>
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
<td>no-regex-spaces</td>
<td>Disallow multiple spaces in a regular expression literal</td>
<td>
<pre>
// Bad
var re = /foo   bar/;
// Good
var re = /foo {3}bar/;
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-regex-spaces)</td>
</tr>
<tr>
<td>no-sparse-arrays</td>
<td>Disallow sparse arrays</td>
<td>
<pre>
var colors = [ "red",, "blue" ];
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-sparse-arrays)</td>
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
<td>no-unreachable</td>
<td>Disallow uinreachable statements after a return, throw, continue, or break statement</td>
<td>
<pre>
function fn() {
    x = 1;
    return x;
    x = 3; // this will never execute
}
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/no-unreachable)</td>
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
<td>use-isnan</td>
<td>Disallow comparisons with the value NaN</td>
<td>
<pre>
if (foo == NaN) {
    // ...
}
if (foo != NaN) {
    // ...
}
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/use-isnan)</td>
</tr>
<tr>
<td>valid-typeof</td>
<td>Ensure that the results of typeof are compared against a valid string</td>
<td>
<pre>
typeof foo === "strnig"
typeof foo == "undefimed"
typeof bar != "nunber"
typeof bar !== "fucntion"
</pre>
</td>
<td>Error</td>
<td>[Link](http://eslint.org/docs/rules/valid-typeof)</td>
</tr>
</tbody>
<table>
