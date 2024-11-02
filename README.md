# Javascript Output Based Question

<details>
 <summary>Notes for Javascript Operator </summary>
 <ul>
  
  **<li>if undefined tries to convert itself into number then it will converted into NaN(Not a number).</li>**
  **<li>If we do comparison of NaN with anyone then we will get false everytime.(EVEN IF WE DO COMPARISON OF NAN WITH NAN , WE WILL GET FALSE )</li>**
  **<li>if any of operand is object or array then they will be converted into primitive(number or string)</li>**  
 **<li> arithmetic + operator </li>**
 
<ul>
  <li>if any of the operand is string then the + operator will concatenate both the operands.</li>
  <li>else the addition will be done and for this the operand will be first converted into numbers and then addition will take place.</li>
</ul>

**<li>arithmetic - operator</li>**
<ul>
  <li>In JavaScript, when the subtraction operator - is used, the operands are converted to numbers before performing the subtraction</li>
</ul>

**<li>Comparison > operator or Comparions < operator</li>**

<ul>
  <li> For > operator Both the operands will be converted into numbers in this case and then comparison of greater than or less than will take plac</li>
</ul>

**<li>Comparison == operator</li>**

<ul>
  <li>The == operator tries to make both the operands of same type if they are not of same type  i.e number type and then do compaison.</li>
  <li>But null and undefined are two operands which will never be converted into numbers in == operator.</li>
  <li>null==null , null==undefined , undefined == undefined (These are the true cases for null and undefined)</li>
</ul>

**<li>Comparison === operator</li>**

<ul>
  <li>It does not do any type conversion and only give true if both the data type and value of operands is same.</li>
  <li>And there is no special case for null and undefined but it was there in == operator.</li>
  <li>/null === null(true) undefined === undefined(true) null === undefined(false)</li>
</ul>
</ul>
</details>

<details>
 <summary>Statement vs Expression</summary>
 <ul>
  <li>Expression:-We can store the result of Expression in a variable.example:-Ternary operator,Function Expression,Function Calling,Operator based expressions ,Array forEach Loop.</li>
  <li>Statement:-We can not store the result of Statement in a variable and if we try to do this we will get Error.examples:-IfElse statement,for loop,Switch,Vairable Declaration.</li>
 </ul>
</details>
 

---
**1. What will be the output**
```js
let a = undefined;
let b = 10;
let c = a + b;
console.log(c);
```

<details>
<summary><b>View Answer</b></summary>
<ul>	
<li><b>Output</b> : NaN</li>
<li><b>Reason</b> : The output is NaN because adding undefined and 10 results in NaN</li>
</ul>
</details>

**[Scroll to Top](#Javascript-Output-Based-Question)**

**2. What will be the output**
```js
console.log(NaN == NaN);
console.log(NaN === NaN);
console.log(NaN !== NaN);
```

<details>
<summary><b>View Answer</b></summary>
<ul>	
<li><b>Output</b> : false,false,false</li>
<li><b>Reason</b> : All comparisons involving NaN return false.</li>
</ul>
</details>

**[Scroll to Top](#Javascript-Output-Based-Question)**

**3. What will be the output**
```js
let a = { name: "Alice" };
let b = [1, 2, 3];
let c = a + b;
console.log(c);
```

<details>
<summary><b>View Answer</b></summary>
<ul>	
<li><b>Output</b> : [object Object]1,2,3</li>
<li><b>Reason</b> : The object gets converted to "[object Object]", and the array gets converted to "1,2,3".</li>
</ul>
</details>

**[Scroll to Top](#Javascript-Output-Based-Question)**

**4. What will be the output**
```js
let a = 5;
let b = {};
let c = a - b;
console.log(c);
```

<details>
<summary><b>View Answer</b></summary>
<ul>	
<li><b>Output</b> : NaN</li>
<li><b>Reason</b> : The output is NaN because the object is converted to 0, resulting in 5 - 0, which is 5.</li>
</ul>
</details>

**[Scroll to Top](#Javascript-Output-Based-Question)**

**5. What will be the output**
```js
console.log(null == undefined);
console.log(null === undefined);
console.log(null == null);
```

<details>
<summary><b>View Answer</b></summary>
<ul>	
<li><b>Output</b> : true,false,true</li>
<li><b>Reason</b> : 
null == undefined is true because they are considered equal.
null === undefined is false because they are of different types.
null == null is true.
</li>
</ul>
</details>

**[Scroll to Top](#Javascript-Output-Based-Question)**

**6. What will be the output**
```js
let a = 2;
let b = "2";
let c = a + b - a;
console.log(c);
```

<details>
<summary><b>View Answer</b></summary>
<ul>	
<li><b>Output</b> : 20</li>
<li><b>Reason</b> : a + b becomes 2 + "2", resulting in "22" (string concatenation).
Then, "22" - a becomes "22" - 2, which coerces the string back to a number, yielding 20.
</li>
</ul>
</details>

**[Scroll to Top](#Javascript-Output-Based-Question)**

**7. What will be the output**
```js
console.log(typeof (5 + "5"));
console.log(typeof (5 - "5"));
```

<details>
<summary><b>View Answer</b></summary>
<ul>	
<li><b>Output</b> : string,number</li>
<li><b>Reason</b> :5 + "5" results in the string "55", so typeof is string.
5 - "5" coerces the string to a number, resulting in 0, so typeof is number.
</li>
</ul>
</details>

**[Scroll to Top](#Javascript-Output-Based-Question)**

**8. What will be the output**
```js
const result=if(5>4)return "true"
else return "false"
```

<details>
<summary><b>View Answer</b></summary>
<ul>	
<li><b>Output</b> : Syntax Error</li>
<li><b>Reason</b> If else is a statement and we cannot store the result of it in a variable and if we try to store its result we will get syntax error.
</li>
</ul>
</details>

**[Scroll to Top](#Javascript-Output-Based-Question)**

**9. What will be the output**
```js
let x=let y=5;
```

<details>
<summary><b>View Answer</b></summary>
<ul>	
<li><b>Output</b> : Syntax Error</li>
<li><b>Reason</b> Variable Declaration is a statement and we cannot store the result of it in a variable and if we try to store its result we will get syntax error.
</li>
</ul>
</details>

**10. What will be the output**
```js
let result=5>4?"Hello World":"Hello India";
console.log(result)
```

<details>
<summary><b>View Answer</b></summary>
<ul>	
<li><b>Output</b> : Hello World</li>
<li><b>Reason</b> Ternary operator is an expression and thus we can store the result of it in a variable and we wil get Hello World here as output.
</li>
</ul>
</details>

**[Scroll to Top](#Javascript-Output-Based-Question)**

**11. What will be the output**
```js
const user={
firstName:"John"
}
console.log(user.firstName)
console.log(user["firstName"])
console.log(user[firstName])
```

<details>
<summary><b>View Answer</b></summary>
<ul>	
<li><b>Output</b> : John,John,Reference Error</li>
<li><b>Reason</b> user[firstName] expression will look into the global scope for variable firstName and will not able to find any variable with name firstName and thus gives us error.
</li>
</ul>
</details>

**[Scroll to Top](#Javascript-Output-Based-Question)**

**12. What will be the output**
```js
let firstName="myName"
const user={
myName:"John"
}
console.log(user.myName)
console.log(user["myName"])
console.log(user[firstName])
```

<details>
<summary><b>View Answer</b></summary>
<ul>	
<li><b>Output</b> : John,John,John</li>
<li><b>Reason</b> user[firstName] expression will look into the global scope for variable firstName and will be succedd in finding variable with name firstName and thus replace the firstName variable with "myName" and then look into the user object for the key myName and then gives us its value.
</li>
</ul>
</details>

**[Scroll to Top](#Javascript-Output-Based-Question)**

**13. What will be the output**
```js
function multiply(a,b=1){
 console.log(a*b)
}
multiply(5,4);
multiply(5);
multiply(5,null);
multiply(5,"");
multiply(5,"  ");
multiply(5,"hello");
multiply(5,false);
multiply(5,undefined);
```

<details>
<summary><b>View Answer</b></summary>
<ul>	
<li><b>Output</b> : 20,5,0,0,0,NaN,0,5</li>
<li><b>Reason</b> The default value will only be taken if we pass undefined or if we didn't pass the argument.In other cases multiplication will happen after type conversion
</li>
</ul>
</details>

**[Scroll to Top](#Javascript-Output-Based-Question)**

**14. What will be the output**
```js
const person = {
  firstName: 'Tushar',
};
const { lastName="Chawla" } = person;
console.log(lastName);
```

<details>
<summary><b>View Answer</b></summary>
<ul>	
<li><b>Output</b> : Chawla</li>
<li><b>Reason</b> The lastName property is not defined in the person object and the destructuring syntax provides a default value ("Chawla") to be used when the property is missing.
</li>
</ul>
</details>

**[Scroll to Top](#Javascript-Output-Based-Question)**

**15. What will be the output**
```js
const person = {
  firstName: 'Tushar',
};
const { firstName="John" } = person;
console.log(lastName);
```

<details>
<summary><b>View Answer</b></summary>
<ul>	
<li><b>Output</b> : Tushar</li>
<li><b>Reason</b>  The `firstName` property in the `person` object has the value 'Tushar'. The default value "John" is ignored because it only applies when the property does not exist or is `undefined`
</li>
</ul>
</details>

**[Scroll to Top](#Javascript-Output-Based-Question)**
