# ES6-Documentation

<h1> Getting Started</h1>

<h2>What is ES6?</h2>
It is a Scripting Language. ES6 brings many new feature like concept of classes, template tags, arrow functions etc. All of the popular javascript libraries and frameworks like Node.js, ReactJS follow ES6.</br>

<h2>1. let & const</h2>
<h3>Let keyword</h3>
-It is block scope.</br>
-We cannot declare one keyword two times.</br>
-We can just declare the keyword without any initialization.</br>

for eg: </br>
let j,</br>
j=20;</br>
l=30;</br>

eg:let a =20;</br>
if(true)</br>
{</br>
a=30;</br>
console.log(a);`30`</br>
}</br>
console.log(a);`20`</br>
age=70;</br>
console.log(a);`70`</br>

<h3>Const keyword.</h3>
-Value of const cannot be change if we change it will throw runtime error.</br>
eg: const X=1;</br>
X=2; </br>
console.log(X); `error:Assignment to constant variable`</br>
-We should initialize the const variable with value at the time of declaration.</br>


Arrays and objects are of **reference types** .So, const here holds doesn't hold constant values but a pointer to those</br> values which is of constant type.</br>

const AGES=[23,45,39];</br>
console.log(AGES); `[23,45,39]`</br>
AGES.push(25);</br>
console.log(AGES); `[23,45,39,25]`</br>

const OBJ={</br>
age=27;</br>
}</br>
console.log(OBJ); `[object Object]{age:27}`</br>
OBJ.age=29;</br>
console.log(age);`[object Object]{age:29}`</br>

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

<h2>3.Hoisting with let and const</h2> </br>
-Hoisting means initializing the varibale before declaring the type.Works with var but doesn't work with let and const.</br>

age=27;</br>
console.log(age);</br></br>
let age; // age is not defined</br>

function f1()</br>
{</br>
age=27;</br>
}</br>
let age;</br>
f1();</br>
console.log(age);`27`</br>
Works fine because we are decaring the age before calling the function.</br>


<h2>4. Arrow function.</h2>
-An addition in ES6.</br>
-We use => in place of function keyword.</br></br>

when your function just have a single argument then tere is no need to pass it in the parenthesis.</br>
eg:</br>
var fn=(a,b)=>return a+b;</br>
console.log(fn(2,3)); `5`</br>

var fn=(a)=>return a+3;</br>
console.log(fn(5));`8`</br>

<h3>Arrow functions with callback functions</h3>
eg:</br>
setTimeout(()=> console.log("Hello!!"),1000) `after 1000 ms. it will print Hello!!`</br>

<h2>5.Object Literal Expressions</h2></br>

Before ES6 we declare object by the key value pairs. eg.</br>
var name = 'Anna';</br>
var age = 20;</br>

var person{</br
    name: name</br>
    age: age</br>
}</br>
console.log(person);</br>

But by ES6 if we can declare the variables above the object creation. eg.</br>
var firstName = 'Anna';</br>
var age = 20;</br>

var person{</br>
    name,</br>
    age</br>
}</br>
console.log(person);</br>

<h3>Method properties</h3>
When we want the value of a property extracted by a function then we use method property.</br></br>
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
var person={</br>
    name: 'Bob',</br>
    age: 20,</br>
    greet (){</br>
          console.log(this.name+" "+this.age)</br>
    }</br>
}</br>
person.greet();</br>
console.log(person);</br>

key value pairs for properties of object</br>
var person={</br>
    "name": 'Bob',</br>
    age: 20,</br>
    "greet Me" (){</br>
          console.log(this.name+" "+this.age)</br>
    }</br>
}</br>
person["greet Me"]();</br>
console.log(person);</br>

<h2>6. Rest Operator</h2>
When invoking a function, a need sometimes arises to be able to pass in an arbitrary number of arguments, and to process these arguments within the function. This need is handled by the rest function parameters syntax. It provides a way to capture the rest of the arguments after the defined arguments using the syntax shown below. These extra arguments are captured in an array.The rest parameter syntax allows us to represent an indefinite number of arguments as an array. </br>

function sumUp(...toAdd)</br>
{</br>
console.log(toAdd);`[100,10,20]`</br>
let result=0;</br>
for(let i =0;i<toAdd.length;i++)</br>
{</br>
result+=toAdd[i];</br>
}</br>
return result;</br>
}</br>
console.log(sumUp(100,10,20));`130`</br>


<h2>7 Spread Operator</h2>
Spread operator allows an iterable to expand in places where 0+ arguments are expected. It is mostly used in variable array</br> where there is more than 1 values are expected.It allows us the privilege to obtain a list of parameters from an array.</br>

let numbers=[1,2,3,4,5];</br>

console.log(...numbers);`1 2 3 4 5 `</br>

console.log(Math.max(...numbers))`5`</br>

<h2>8. for-of-Loop</h2></br>
for-of is a new loop in ES6 that replaces both for-in and forEach() and supports the new iteration protocol.</br>

let a=[1.29,3.50,7.9];</br>
for(let b of a)</br>
{</br>
console.log(a);`1.29 3.50 7.9` </br>
}</br>


<h2>9. Template Literals</h2>
String templating refers to interpolating variables and expressions into strings using a syntax like perl or the shell. A string template is enclosed in back-tick characters . By contrast single quotes (‘) or double quotes (“) indicate normal strings. Expressions inside the template are marked out between ${ and }. Here is an example:
String Interpolation</br>
Before ES6 we have to concatenate the strings using + symbol.</br>
But now, we can manipulate the strings using ${variable_name} by enclosing the whole expression in backticks .</br>
let name = 'Sara';</br>
let age = 23;</br>
let msg = `My name is ${name} I am ${age}.`</br>
console.log(msg);</br>

Multi line template literals</br>
In JS ES5 we did multi line literals as:</br>
const msg = "Like\n" +</br>
"this !1\n"</br>
console.log(msg);</br>

But by ES6 we have multi line template literals . To have multi line literals use backticks .</br>
const msg = `Like </br>
this !!.`</br>
console.log(msg);</br>

<h2>10. Destructuring Arrays.</h2>
Destructuring is a JavaScript expression that makes it possible to unpack values from arrays, or properties from objects,</br> into distinct variables.</br>

Traditional way of fetching values from Array.</br>
let numbers=[1,2,3];</br>

console.log(numbers[0],numbers[1]);</br>

With ES6 approach</br>

let numbers=[1,2,3];</br>
let[a, ,c]=numbers;</br>
console.log(a, c);`1 3`</br>
let[a,b]=numbers;</br>
console.log(a);`1`</br>
console.log(b);`2`</br>
let[a,b,c,d]=numbers;</br>
console.log(d);`undefined`</br>


with Rest parameters</br>

let numbers=[1,2,"3"];</br>
let[a,...b]=numbers;</br>
consol[a,b,c,d=10]=numbers;</br>
console.log(d);//10</br>

Swapping values</br>
let a =5;</br>
let b =10;</br>
[b,a]=[a,b];</br>
console.log(a);`10`</br>
console.log(b);`5`


