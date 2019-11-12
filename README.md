# ES6-Documentation

<h1> Getting Started</h1>

<h2>What is ES6?</h2>
It is a Scripting Language. ES6 brings many new feature like concept of classes, template tags, arrow functions etc. All of the popular javascript libraries and frameworks like Node.js, ReactJS follow ES6.</br>

<h2>1. let & const</h2>
<h3>Let keyword</h3>
-It is block scope.</br>
-We cannot declare one keyword two times.</br>
-We can just declare the keyword without any initialization.</br>

*eg: </br>
let j,</br>
j=20;</br>
j=30;</br>*

*eg:
let a =20;</br>
if(true)</br>
{</br>
a=30;</br>
console.log(a);`30`</br>
}</br>
console.log(a);`20`</br>
age=70;</br>
console.log(a);`70`</br>*

<h3>Const keyword.</h3>
-Value of const cannot be change if we change it will throw runtime error.</br>
eg: const X=1;</br>
X=2; </br>
console.log(X);`error:Assignment to constant variable`</br>
-We should initialize the const variable with value at the time of declaration.</br>

Arrays and objects are of **reference types** .So, const here holds doesn't hold constant values but a pointer to those</br> values which is of constant type.</br>

*eg:const AGES=[23,45,39];</br>
console.log(AGES); `[23,45,39]`</br>
AGES.push(25);</br>
console.log(AGES); `[23,45,39,25]`</br>*

*eg:const OBJ={</br>
age=27;</br>
}</br>
console.log(OBJ); `[object Object]{age:27}`</br>
OBJ.age=29;</br>
console.log(age);`[object Object]{age:29}`</br>*

<h2>2. Block Scope</h2>
-Anything within{} is considered to be block scope. </br>
-let and const both are block scope variables.</br>
eg:</br>
let y=9;</br>
if(3>2)</br>
{</br>
y=10;</br>
console.log(y);`10`</br>
}</br>
console.log(y);`9`</br>

<h2>3.Hoisting with let and const</h2> 
-Hoisting means initializing the varibale before declaring the type.Works with var but doesn't work with let and const.</br>
eg:age=27;</br>
console.log(age);</br>
let age; `age is not defined`</br>

*function f1()</br>
{</br>
age=27;</br>
}</br>
let age;</br>
f1();</br>
console.log(age);`27`</br>*
Works fine because we are decaring the age before calling the function.</br>

<h2>4. Arrow function.</h2>
-An addition in ES6.</br>
-We use => in place of function keyword.</br></br>
Math
when your function just have a single argument then tere is no need to pass it in the parenthesis.</br>
*eg:</br>
var fn=(a,b)=>return a+b;</br>
console.log(fn(2,3)); `5`</br>*

*eg:var fn=(a)=>return a+3;</br>
console.log(fn(5));`8`</br>*

<h3>Arrow functions with callback functions</h3>
eg:</br>
setTimeout(()=> console.log("Hello!!"),1000) `after 1000 ms. it will print Hello!!`

<h2>5.Object Literal Expressions</h2>
Before ES6 we declare object by the key value pairs. 
eg.</br>
var name = 'Anna';</br>
var age = 20;</br>
var person{</br
    name: name</br>
    age: age</br>
}</br>
console.log(person);</br>

But by ES6 if we can declare the variables above the object creation. *eg.</br>
var firstName = 'Anna';</br>
Terms
Privacy
Security
Status
Help
var age = 20;</br>
var person{</br>
    name,</br>
    age</br>
}</br>
console.log(person);</br>*

<h3>Method properties</h3>
When we want the value of a property extracted by a function then we use method property.</br>
var person={</br>
    name: 'Bob',</br>
    age: 20,</br>
    greet: function(){</br>
        console.log(this.name+" "+this.age)</br>
    }</br>
}</br>
person.greet();</br>
console.log(person);</br>

But from ES6 this also become very concise .</br>

*var person={</br>
    name: 'Bob',</br>
    age: 20,</br>
    greet (){</br>
          console.log(this.name+" "+this.age)</br>
    }</br>
}</br>
person.greet();</br>
console.log(person);</br>*

key value pairs for properties of object</br>
*var person={</br>
    "name": 'Bob',</br>
    age: 20,</br>
    "greet Me" (){</br>
          console.log(this.name+" "+this.age)</br>
    }</br>
}</br>
person ["greet Me"] ();</br>
console.log(person);</br>*

<h2>6. Rest Operator</h2>
When invoking a function, a need sometimes arises to be able to pass in an arbitrary number of arguments, and to process these arguments within the function. This need is handled by the rest function parameters syntax. It provides a way to capture the rest of the arguments after the defined arguments using the syntax shown below. These extra arguments are captured in an array.The rest parameter syntax allows us to represent an indefinite number of arguments as an array. </br>

*eg:function sumUp(...toAdd)</br>
{</br>
console.log(toAdd);`[100,10,20]`</br>
let result=0;</br>
for(let i =0;i<toAdd.length;i++)</br>
{</br>
result+=toAdd[i];</br>
}</br>
return result;</br>
}</br>
console.log(sumUp(100,10,20));`130`</br>*


<h2>7 Spread Operator</h2>
Spread operator allows an iterable to expand in places where 0+ arguments are expected. It is mostly used in variable array</br> where there is more than 1 values are expected.It allows us the privilege to obtain a list of parameters from an array.</br>

*eg:let numbers=[1,2,3,4,5];</br>
console.log(...numbers);`1 2 3 4 5 `</br>
console.log(Math.max(...numbers))`5`</br>*

<h2>8. for-of-Loop</h2>
for-of is a new loop in ES6 that replaces both for-in and forEach() and supports the new iteration protocol.</br>

*eg:let a=[1.29,3.50,7.9];</br>
for(let b of a)</br>
{</br>
console.log(a);`1.29 3.50 7.9` </br>
}</br>*


<h2>9. Template Literals</h2>
String templating refers to interpolating variables and expressions into strings using a syntax like perl or the shell. A string template is enclosed in back-tick characters . By contrast single quotes (‘) or double quotes (“) indicate normal strings. Expressions inside the template are marked out between ${ and }. Here is an example:
String Interpolation</br>
Before ES6 we have to concatenate the strings using + symbol.</br>
But now, we can manipulate the strings using ${variable_name} by enclosing the whole expression in backticks .</br>

*eg:let name = 'Sara';</br>
let age = 23;</br>
let msg = `My name is ${name} I am ${age}.`</br>
console.log(msg);</br>*

Multi line template literals</br>
In JS ES5 we did multi line literals as:</br>

*eg:const msg = "Like\n" +</br>
"this !1\n"</br>
console.log(msg);</br>*

But by ES6 we have multi line template literals . To have multi line literals use backticks .</br>

*eg:const msg = `Like </br>
this !!.`</br>
console.log(msg);</br>*

<h2>10. Destructuring Arrays.</h2>
Destructuring is a JavaScript expression that makes it possible to unpack values from arrays, or properties from objects,</br> into distinct variables.</br>

Traditional way of fetching values from Array.</br>
*eg:let numbers=[1,2,3];</br>
console.log(numbers[0],numbers[1]);</br>*

With ES6 approach</br>
*let numbers=[1,2,3];</br>
let[a, ,c]=numbers;</br>
console.log(a, c);`1 3`</br>
let[a,b]=numbers;</br>
console.log(a);`1`</br>
console.log(b);`2`</br>
let[a,b,c,d]=numbers;</br>
console.log(d);`undefined`</br>*

With Rest parameters</br>
*let numbers=[1,2,"3"];</br>
let[a,...b]=numbers;</br>
consol[a,b,c,d=10]=numbers;</br>
console.log(d);`10`</br>*

Swapping values</br>
*let a =5;</br>
let b =10;</br>
[b,a]=[a,b];</br>
console.log(a);`10`</br>
console.log(b);`5`*

<h2>11. tag</h2></br>
Allows us to fetch String and values separately</br>
 function tag(strings, ...values) {</br>
  console.log(strings);`[ 'My name \n is ', '  and my age is ', '' ]`</br>
  console.log(values);`[ 'Apoorva', 23 ]`</br>
}</br>

 const name = "Apoorva";</br>
 const age = 23;</br>
 tag`My name \n is ${name}  and my age is ${age}`;</br>


<h2>12.Generators</h2>
A generator is a function that can stop midway and can continue from where it stopped.</br>

function* fibonacci() {</br>
  let n1 = 0;</br>
  let n2 = 1;</br>
  while (true) </br>
  {</br>
    let current = n1;</br>
    n1 = n2;</br>
    n2 = current + n1;</br>
    yield current;</br>
  }</br>
}</br>

const iter = fibonacci(); </br>
console.log(iter.next()); `{ value: 0, done: false }`</br>
console.log(iter.next()); `{ value: 1, done: false }`</br>
console.log(iter.next()); `{ value: 1, done: false }`</br>
console.log(iter.next()); `{ value: 2, done: false }`</br>
console.log(iter.next()); `{ value: 3, done: false }`</br>
console.log("Stop here"); `Stop here`</br>
console.log(iter.next()); `{ value: 5, done: false }`</br>
console.log(iter.next()); `{ value: 8, done: false }`</br>
console.log(iter.next()); `{ value: 13, done: false }`</br>

<h2>13. Object Assignment</h2>

var obj1 = {</br>
  skill: {</br>
    running: true</br>
  }</br>
};</br>

var obj2 = {</br>
  name: "Apoorva"</br>
};</br>

obj1 = obj2;</br>
console.log(obj1); `{ name: 'Apoorva' }`</br>

Object.assign(obj1, obj2);</br>
console.log(obj1); `{ skill: { running: true }, name: 'Apoorva' }`</br>

Object.keys(obj2).forEach(key => {</br>
  obj1[key] = obj2[key];</br>
});</br>
console.log(obj1);  `{ skill: { running: true }, name: 'Apoorva' }`</br>

<h2>14. Array Methods</h2>

<h3>startsWith()</h3>
const startsWith = "helloWorld".startsWith("hello");</br>
console.log(startsWith); `true`</br>

<h3>endsWith()</h3>
const endsWith = "helloWorld".endsWith("World");</br>
console.log(endsWith); `true`</br>

<h3>repeat()</h3>
const string = "#".repeat(9);</br>
console.log(string); `#########`</br>
 
<h3>includes()</h3>
const includes = "helloworld".includes("llo");</br>
console.log(includes); `true`</br>
 
<h3>findIndex()</h3>
var arr = [1, 12, 30, 5, 6];</br>
const results = arr.findIndex(function(index) {</br>
  return index > 10;</br>
});</br>
console.log(results); `1`</br>

<h3>find()</h3>
var arr = [1, 12, 30, 5, 6];</br>
const results = arr.find(function(number) {</br>
  return number > 20;</br>
});</br>
console.log(results); `30`</br>

<h2>15. Math functions</h2>
<h3>trunc() </h3>
returns the whole number by removing the fractional part.</br>
var number = 98.9;</br>
console.log(Math.trunc(number)); `98`</br>

<h3>sign()</h3>
console.log(Math.sign(10)); `1`</br>
console.log(Math.sign(-23)); `-1`</br>
console.log(Math.sign(0)); `0`</br>

<h2>16. Number methods </h2>
<h3>isNaN()</h3></br>
Returns false if number.Returns true if not a number.</br>




















ar number=98.9;</br>
console.log(Number.isNaN(98.9)); `false`</br>

<h3>isFinite()</h3>
Returns true if number is not otherwise false.</br>
var i = 1 / 0;v
console.log(Number.isFinite(i));`false`</br>

<h3>isSafeInteger()</h3>
Returns true if integer is safe, else false.</br>
console.log(Number.isSafeInteger(1e1000));`false`</br>




