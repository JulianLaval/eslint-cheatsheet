### Stylistic Issues
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
<td>array-bracket-spacing</td>
<td>Enfore spacing inside array brackets</td>
<td>
<pre>
var arr = [ 'foo', 'bar' ];
var [ x, y ] = z;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/array-bracket-spacing)</td>
</tr>
<tr>
<td>brace-style</td>
<td>Enfore one true brace style</td>
<td>
<pre>
if (foo) {
} else {
}
------------
if (foo) {   
} 
else {
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/brace-style)</td>
</tr>
<tr>
<td>camelcase</td>
<td>Require camel case names</td>
<td>
<pre>
variableName vs variable_name
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/camelcase)</td>
</tr>
<tr>
<td>comma-spacing</td>
<td>Enfore spacing before and after comma</td>
<td>
<pre>
var foo = 1, bar = 2;
var foo = 1 ,bar = 2;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/comma-spacing)</td>
</tr>
<tr>
<td>comma-style</td>
<td>Enfore one true comma style</td>
<td>
<pre>
var foo = 1
, //lone comma
bar = 2;

var foo = 1
  , bar = 2;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/comma-style)</td>
</tr>
<tr>
<td>computed-property-spacing</td>
<td>Require or disallow padding inside computed properties</td>
<td>
<pre>
obj[foo]
obj[ foo ]
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/computed-property-spacing)</td>
</tr>
<tr>
<td>consistent-this</td>
<td>Enfore consistent naming when capturing the current execution context</td>
<td>
<pre>
// If alias is set to "self", the following are errors
var self = 42;
var that = this;
self = 42;
that = this;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/consistent-this)</td>
</tr>
<tr>
<td>eol-last</td>
<td>Enfore newline at the end of file, with no multiple empty lines</td>
<td>
<pre>
function doSmth() {
  ...
}
// no space here
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/eol-last)</td>
</tr>
<tr>
<td>func-names</td>
<td>Require function expressions to have a name</td>
<td>
<pre>
// Bad
Foo.prototype.bar = function() {};
(function() {
    // ...
}())
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/func-names)</td>
</tr>
<tr>
<td>func-style</td>
<td>Enfore use of function declarations or expressions</td>
<td>
<pre>
function doSomething() {
    // ...
}
----
var doSomething = function() {
    // ...
};
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/func-style)</td>
</tr>
<tr>
<td>id-length</td>
<td>This option enforces minimum and maximum identifier lengths</td>
<td>
<pre>
// id-length: 1  // default is minimum 2-chars ({ min: 2})
var x = 5; // too short
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/id-length)</td>
</tr>
<tr>
<td>id-match</td>
<td>Require identifiers to match the provided regular expression</td>
<td>
<pre>

</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/id-match)</td>
</tr>
<tr>
<td>indent</td>
<td>Specify tab or space width for your code</td>
<td>
<pre>

</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/indent)</td>
</tr>
<tr>
<td>key-spacing</td>
<td>Enforce spacing between keys and values in object literal properties</td>
<td>
<pre>
// key-spacing beforeColon & afterColon = false
var obj = { foo:42 };
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/key-spacing)</td>
</tr>
<tr>
<td>lines-around-comment</td>
<td>Enfore empty lines around comments</td>
<td>
<pre>
// beforeBlockComment only
var x = 0;

/* the vertical position */
var y = 10;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/lines-around-comment)</td>
</tr>
<tr>
<td>linebreak-style</td>
<td>Disallow mixed 'LF' and 'CLRF' as linebreaks</td>
<td>
<pre>
    var a = 'a',\r\n // unix
        b = 'b';\n // windows
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/linebreak-style)</td>
</tr>
<tr>
<td>max-nested-callbacks</td>
<td>Specify the maximum depth callbacks can be nested</td>
<td>
<pre>
foo(function () {
    bar(function () {
        baz(function() {
            qux(function () {
            });
        });
    });
});
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/max-nested-callbacks)</td>
</tr>
<tr>
<td>new-cap</td>
<td>Require a capital letter for constructors</td>
<td>
<pre>
// Bad
var friend = new person();
var colleague = Person();
// Good
var friend = new Person();
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/new-cap)</td>
</tr>
<tr>
<td>new-parens</td>
<td>Disallow the omission of parentheses when invoking a constructor with no arguments</td>
<td>
<pre>
var person = new Person;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/new-parens)</td>
</tr>
<tr>
<td>newline-after-var</td>
<td>Require or disallow an empty newline after variable declarations</td>
<td>
<pre>
var foo;

// do something with foo
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/newline-after-var)</td>
</tr>
<tr>
<td>no-array-constructor</td>
<td>Disallow use of the `Array` constructor</td>
<td>
<pre>
new Array(0, 1, 2)
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-array-constructor)</td>
</tr>
<tr>
<td>no-continue</td>
<td>Disallow use of the `continue` statement</td>
<td>
<pre>
var sum = 0,
    i;

for(i = 0; i < 10; i++) {
    if(i >= 5) {
        continue;
    }
    a += i;
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-continue)</td>
</tr>
<tr>
<td>no-inline-comments</td>
<td>Disallow comments inline after code</td>
<td>
<pre>
var a = 1; // declaring a to 1
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-inline-comments)</td>
</tr>
<tr>
<td>no-lonely-if</td>
<td>Disallow `if` as the only statement in an `else` block</td>
<td>
<pre>
if (...) {
    ...
} else {
    if (...) {
        ...
    }
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-lonely-if)</td>
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
<td>no-multiple-empty-lines</td>
<td>Disallow multiple empty lines</td>
<td>
<pre>
// no-multiple-empty-lines: [1, {max: 2}]  // Maximum of 2 empty lines.
var foo = 5;


var bar = 3;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-multiple-empty-lines)</td>
</tr>
<tr>
<td>no-nested-ternary</td>
<td>Disallow nested  ternary expressions</td>
<td>
<pre>
var foo = bar ? baz : qux === quxx ? bing : bam;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-nested-ternary)</td>
</tr>
<tr>
<td>no-new-object</td>
<td>Disallow the use of the `Object` constructor</td>
<td>
<pre>
// Bad
var myObject = new Object();
// Good
var myObject = {};
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-new-object)</td>
</tr>
<tr>
<td>no-spaced-func</td>
<td>Disallow space between function identifier and application</td>
<td>
<pre>
fn () vs fn()
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-spaced-func)</td>
</tr>
<tr>
<td>no-ternary</td>
<td>Disallow the use of ternary operators</td>
<td>
<pre>
var foo = isBar ? baz : qux;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-ternary)</td>
</tr>
<tr>
<td>no-trailing-spaces</td>
<td>Disallow trailing whitespace at the end of lines</td>
<td>
<pre>
// spaces, tabs and unicode whitespaces
// are not allowed at the end of lines
var foo = 0;•••••
var baz = 5;••
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-trailing-spaces)</td>
</tr>
<tr>
<td>no-underscore-dangle</td>
<td>Disallow dangling underscores in identifiers</td>
<td>
<pre>
var _foo;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-underscore-dangle)</td>
</tr>
<tr>
<td>no-unneeded-ternary</td>
<td>Disallow the use of `Boolean` literals in conditional expressions</td>
<td>
<pre>
// Bad
var isYes = answer === 1 ? true : false;
// Good
var isYes = answer === 1;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/no-unneeded-ternary)</td>
</tr>
<tr>
<td>object-curly-spacing</td>
<td>Require or disallow padding inside curly braces</td>
<td>
<pre>
var obj = { foo: "bar" };

var obj = {foo: "bar"};
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/object-curly-spacing)</td>
</tr>
<tr>
<td>one-var</td>
<td>Require or disallow one variable declaration per function</td>
<td>
<pre>
// one variable declaration per function
function foo() {
    var bar, baz;
}
// multiple variable declarations per function
function foo() {
    var bar;
    var baz;
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/one-var)</td>
</tr>
<tr>
<td>operator-assignment</td>
<td>Require assignment operator shorthand where possible or prohibit it entirely</td>
<td>
<pre>
x += y;

x = x + y;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/operator-assignment)</td>
</tr>
<tr>
<td>operator-linebreak</td>
<td>Enfore operators to be placed before or after line breaks</td>
<td>
<pre>
var fullHeight = borderTop +
                 innerHeight +
                 borderBottom;

var fullHeight = borderTop
               + innerHeight
               + borderBottom;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/operator-linebreak)</td>
</tr>
<tr>
<td>padded-blocks</td>
<td>Enfore padding within blocks</td>
<td>
<pre>
if (a) {
    b();
}

if (a) {

    b();

}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/padded-blocks)</td>
</tr>
<tr>
<td>quote-props</td>
<td>Require quotes around object literal property names</td>
<td>
<pre>
var object1 = {
    property: true;
};

var object2 = {
    "property": true
};
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/quote-props)</td>
</tr>
<tr>
<td>quotes</td>
<td>Specify whether backticks, double or single quotes should be used</td>
<td>
<pre>
var double = "double";
var single = 'single';
var backtick = `backtick`;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/quotes)</td>
</tr>
<tr>
<td>semi-spacing</td>
<td>Enfore spacing before and after semicolons</td>
<td>
<pre>
var a = "b" ;

var c = "d";var e = "f";
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/semi-spacing)</td>
</tr>
<tr>
<td>sort-vars</td>
<td>Sort variables within the same declaration block</td>
<td>
<pre>
var b, a;

var a, B, c;

var a, A;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/sort-vars)</td>
</tr>
<tr>
<td>space-after-keywords</td>
<td>Require a space after certain keywords</td>
<td>
<pre>
if (condition) {
    doSomething();
} else {
    doSomethingElse();
}

if(condition) {
    doSomething();
}else{
    doSomethingElse();
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/space-after-keywords)</td>
</tr>
<tr>
<td>space-before-blocks</td>
<td>Require or disallow a space before blocks</td>
<td>
<pre>
if (a){

if (a) {
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/space-before-blocks)</td>
</tr>
<tr>
<td>space-before-function-paren</td>
<td>Require or disallow a space before function opening parenthesis</td>
<td>
<pre>
function withoutSpace(x) {
}

function withSpace (x) {
}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/space-before-function-paren)</td>
</tr>
<tr>
<td>space-in-parens</td>
<td>Require or disallow spaces inside parentheses</td>
<td>
<pre>
foo( 'bar' );
var x = ( 1 + 2 ) * 3;

foo('bar');
var x = (1 + 2) * 3;
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/space-in-parens)</td>
</tr>
<tr>
<td>space-infix-ops</td>
<td>Require spaces around operators</td>
<td>
<pre>
a+b
a +b
a+ b
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/space-infix-ops)</td>
</tr>
<tr>
<td>space-return-throw-case</td>
<td>Require a space after `return`, `throw`, and `case`</td>
<td>
<pre>
throw{a:0}
throw {a:0}
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/space-return-throw-case)</td>
</tr>
<tr>
<td>space-unary-ops</td>
<td>Require or disallow spaces before/after unary operators</td>
<td>
<pre>
foo++
foo ++
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/space-unary-ops)</td>
</tr>
<tr>
<td>spaced-comment</td>
<td>Require or disallow a space immediately following the `//` or `/*` in a comment</td>
<td>
<pre>
//Comment
// Comment
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/spaced-comment)</td>
</tr>
<tr>
<td>wrap-regex</td>
<td>Require regex literals to be wrapped in parentheses</td>
<td>
<pre>
return /foo/.test("bar");
return (/foo/).test("bar");
</pre>
</td>
<td>Off</td>
<td>[Link](http://eslint.org/docs/rules/wrap-regex)</td>
</tr>
</tbody>
<table>
