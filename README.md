# ES6-Documentation

<h1> Getting Started</h1>

<h2>What is ES6?<h2>
It is a Scripting Language.

1. let & const

Let keyword
It is block scope
We cannot declare one keyword two times.
We can just declare the keyword without any initialization.

for eg: 
let j,
j=20;
l=30;

Explanation by Code 
let a =20;
if(true)
{
a=30;
console.log(a); //30
}
console.log(a);//20
age=70;
console.log(a);//70


Const keyword.
Value of const cannot be change if we change it will throw runtime error.
eg: const X=1;
X=2; 
console.log(X); //error:Assignment to constant variable
We should initialize the const variable with value at the time of declaration.


Arrays and objects are of **reference types** .So, const here holds doesn't hold constant values but a pointer to those values which is of constant type.

const AGES=[23,45,39];
console.log(AGES); //[23,45,39]
AGES.push(25);
console.log(AGES); //[23,45,39,25]

const OBJ={
age=27;
}
console.log(OBJ); //[object Object]{age:27}
OBJ.age=29;
console.log(age);//[object Object]{age:29}

2. Block Scope
Anuthing within{} is considered to be block scope. 
let and const both are block scope variables

eg:
let y=9;
if(3>2)
{
y=10;
console.log(y);//10
}
console.log(y)//9

3.Hoisting with let and const 
Hoisting means initializing the varibale before declaring the type.Works with var but doesn't work with let and const.

age=27;
console.log(age);
let age; // age is not defined

function f1()
{
age=27;
}
let age;
f1();
console.log(age);// 27
Works fine because we are decaring the age before calling the function.


4. Arrow function.
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

eg:
let name ="Anna"
let age=25;
let obj={
name,
age
}
console.log(obj);//[object Object]{age:25,name:Anna}

It will automatically look if  it has the value of the variables decalred before declaration of the Object
