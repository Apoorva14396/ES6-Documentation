# ES6-Documentation

<h1> Getting Started</h1></br>

<h2>What is ES6?</h2></br>
It is a Scripting Language.</br>

1. let & const</br>

Let keyword</br>
It is block scope.</br>
We cannot declare one keyword two times.</br>
We can just declare the keyword without any initialization.</br>

for eg: </br>
let j,</br>
j=20;</br>
l=30;</br>

eg:let a =20;</br>
if(true)</br>
{</br>
a=30;</br>
console.log(a);//30</br>
}</br>
console.log(a);//20</br>
age=70;</br>
console.log(a);//70</br>


Const keyword.</br>
Value of const cannot be change if we change it will throw runtime error.</br>
eg: const X=1;</br>
X=2; </br>
console.log(X); //error:Assignment to constant variable</br>
We should initialize the const variable with value at the time of declaration.</br>


Arrays and objects are of **reference types** .So, const here holds doesn't hold constant values but a pointer to those</br> values which is of constant type.</br>

const AGES=[23,45,39];</br>
console.log(AGES); //[23,45,39]</br>
AGES.push(25);</br>
console.log(AGES); //[23,45,39,25]</br>

const OBJ={</br>
age=27;</br>
}</br>
console.log(OBJ); //[object Object]{age:27}</br>
OBJ.age=29;</br>
console.log(age);//[object Object]{age:29}</br>

2. Block Scope</br>
Anuthing within{} is considered to be block scope. </br>
let and const both are block scope variables.</br>

eg:</br>
let y=9;</br>
if(3>2)</br>
{</br>
y=10;</br>
console.log(y);//10</br>
}</br>
console.log(y)//9</br>

3.Hoisting with let and const </br>
Hoisting means initializing the varibale before declaring the type.Works with var but doesn't work with let and const.</br>

age=27;</br>
console.log(age);</br></br>
let age; // age is not defined</br>

function f1()</br>
{</br>
age=27;</br>
}</br>
let age;</br>
f1();</br>
console.log(age);// 27</br>
Works fine because we are decaring the age before calling the function.</br>


4. Arrow function.</br>
An addition in ES6.
We use => in place of function keyword.

when your function just have a single argument then tere is no need to pass it in the parenthesis.
eg:
var fn=(a,b)=>return a+b;
console.log(fn(2,3)); //5

var fn=(a)=>return a+3;
console.log(fn(5)); //8

<h2>Arrow functions with callback functions</h2>
eg:
setTimeout(()=> console.log("Hello!!"),1000) // after 1000 ms. it will print Hello!!

5.Object Literal Expressions

Before ES6 we declare object by the key value pairs. eg.
var name = 'Anna';
var age = 20;

var person{
    name: name,
    age: age
}
console.log(person);

But by ES6 if we can declare the variables above the object creation. eg.
var firstName = 'Anna';
var age = 20;

var person{
    name,
    age
}
console.log(person);

Method properties

When we want the value of a property extracted by a function then we use method property.
var person={
    name: 'Bob',
    age: 20,
    greet: function(){
        console.log(this.name+" "+this.age)
    }
}
person.greet();
console.log(person);

But from ES6 this also become very concise .
var person={
    name: 'Bob',
    age: 20,
    greet (){
          console.log(this.name+" "+this.age)
    }
}
person.greet();
console.log(person);


key value pairs for properties of object
var person={
    "name": 'Bob',
    age: 20,
    "greet Me" (){
          console.log(this.name+" "+this.age)
    }
}
person["greet Me"]();
console.log(person);


Dynamically adding property names

let name='Anna';
let age =25;

let ageField="age";
let obj={
"name":'Sara',
[ageField]: 28,
    "greet Me" (){
          console.log(this.name+" "+this.age)
    }
}
console.log(obj);

6. Rest Operator
The rest parameter syntax allows us to represent an indefinite number of arguments as an array. 

function sumUp(...toAdd)
{
console.log(toAdd);//[100,10,20]
let result=0;
for(let i =0;i<toAdd.length;i++)
{
result+=toAdd[i];
}
return result;
}
console.log(sumUp(100,10,20)); //130


7 Spread Operator
Spread operator allows an iterable to expand in places where 0+ arguments are expected. It is mostly used in variable array where there is more than 1 values are expected.It allows us the privilege to obtain a list of parameters from an array.

let numbers=[1,2,3,4,5];

console.log(...numbers);// 1 2 3 4 5 

console.log(Math.max(...numbers))//5

8. for-of-Loop
for-of is a new loop in ES6 that replaces both for-in and forEach() and supports the new iteration protocol.

let a=[1.29,3.50,7.9];
for(let b of a)
{
console.log(a);// 1.29 3.50 7.9 
}


9. Template Literals
String Interpolation
Before ES6 we have to concatenate the strings using + symbol.
But now, we can manipulate the strings using ${variable_name} by enclosing the whole expression in backticks .
let name = 'Sara';
let age = 23;
let msg = `My name is ${name} I am ${age}.`
console.log(msg);

Multi line template literals
In JS ES5 we did multi line literals as:
const msg = "Like\n" +
"this !1\n"
console.log(msg);

But by ES6 we have multi line template literals . To have multi line literals use backticks .
const msg = `Like 
this !!.`
console.log(msg);

10. Destructuring Arrays.
Destructuring is a JavaScript expression that makes it possible to unpack values from arrays, or properties from objects, into distinct variables.

Traditional way of fetching values from Array.
let numbers=[1,2,3];

console.log(numbers[0],numbers[1]);

With ES6 approach

let numbers=[1,2,3];
let[a, ,c]=numbers;
console.log(a, c);//1 3
let[a,b]=numbers;
console.log(a);//1
console.log(b);//2
let[a,b,c,d]=numbers;
console.log(d);//undefined


with Rest parameters

let numbers=[1,2,"3"];
let[a,...b]=numbers;
consol[a,b,c,d=10]=numbers;
console.log(d);//10

Swapping values
let a =5;
let b =10;
[b,a]=[a,b];
console.log(a);//10
console.log(b);//5


