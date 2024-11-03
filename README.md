# Javascript Output Based Question

<details>
 <summary>Type Conversion</summary>
 <table>
  <tr>
   <th></th>
   <th>Boolean</th>
   <th>String</th>
   <th>Number</th>
  </tr>
  <tr>
   <td>""</td>
   <td>false</td>
   <td>""</td>
   <td>0</td>
  </tr>
  <tr>
   <td>"  "</td>
   <td>true</td>
   <td>"  "</td>
   <td>0</td>
  </tr>
  <tr>
   <td>"5"</td>
   <td>true</td>
   <td>"5"</td>
   <td>5</td>
  </tr>
  <tr>
   <td>"5hello"</td>
   <td>true</td>
   <td>"5hello"</td>
   <td>NaN</td>
  </tr>
 </table>

 <table>
  <tr>
   <th></th>
   <th>Boolean</th>
   <th>String</th>
   <th>Number</th>
  </tr>
  <tr>
   <td>0</td>
   <td>false</td>
   <td>"0"</td>
   <td>0</td>
  </tr>
  <tr>
   <td>-0</td>
   <td>false</td>
   <td>"-0"</td>
   <td>-0</td>
  </tr>
  <tr>
   <td>1</td>
   <td>true</td>
   <td>"1"</td>
   <td>1</td>
  </tr>
  <tr>
   <td>-1</td>
   <td>true</td>
   <td>"-1"</td>
   <td>-1</td>
  </tr>
  <tr>
   <td>Infinity</td>
   <td>true</td>
   <td>"Infinity"</td>
   <td>Infinity</td>
  </tr>
   <tr>
   <td>-Infinity</td>
   <td>true</td>
   <td>"-Infinity"</td>
   <td>-Infinity</td>
  </tr>
   <tr>
   <td>NaN</td>
   <td>false</td>
   <td>"NaN"</td>
   <td>NaN</td>
  </tr>
 </table>

 <table>
  <tr>
   <th></th>
   <th>Boolean</th>
   <th>String</th>
   <th>Number</th>
  </tr>
  <tr>
   <td>null</td>
   <td>false</td>
   <td>"null"</td>
   <td>0</td>
  </tr>
  <tr>
   <td>undefined</td>
   <td>false</td>
   <td>"undefined"</td>
   <td>NaN</td>
  </tr>
 </table>

 <table>
  <tr>
   <th></th>
   <th>Boolean</th>
   <th>String</th>
   <th>Number</th>
  </tr>
  <tr>
   <td>[]</td>
   <td>true</td>
   <td>""</td>
   <td>0</td>
  </tr>
  <tr>
   <td>{}</td>
   <td>true</td>
   <td>"[object Object]"</td>
   <td>NaN</td>
  </tr>
  <tr>
   <td>["1"]</td>
   <td>true</td>
   <td>"1"</td>
   <td>1</td>
  </tr>
   <tr>
   <td>["1","2"]</td>
   <td>true</td>
   <td>"1,2"</td>
   <td>NaN</td>
  </tr>
   <tr>
   <td>[1,"2",[3,4],5,6,[],7,8,{},{age:21}]</td>
   <td>true</td>
   <td>"1,2,3,4,5,6,,7,8,[object Object],[object Object]"</td>
   <td>NaN</td>
  </tr>
 </table>
 
</details>

<details>
 <summary>Notes for Javascript Operator </summary>
 <ul>
  
  **<li>if undefined tries to convert itself into number then it will converted into NaN(Not a number).</li>**
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

**<li>Comparison === operator</li>**

<ul>
  <li>It does not do any type conversion and only give true if both the data type and value of operands is same.</li>
  <li>And there is no special case for null and undefined but it was there in == operator.</li>
  <li>/null === null(true) undefined === undefined(true) null === undefined(false)</li>
</ul>

**<li>Comparison == operator</li>**

<ul>
<!--   <li>The == operator tries to make both the operands of same type if they are not of same type  i.e number type and then do compaison.</li>
  <li>But null and undefined are two operands which will never be converted into numbers in == operator.</li>
  <li>null==null , null==undefined , undefined == undefined (These are the true cases for null and undefined)</li> -->
 
 1. If the types are the same:If both operands are of the same type, == simply checks for equality without any type conversion.
Example: "5" == "5" is true, and 5 == 5 is true.

2. If one operand is null and the other is undefined:
JavaScript treats null and undefined as equal.
So null == undefined is true, but they are not coerced to any other type.
Example: null == undefined → true.

3. If one operand is a number and the other is a string:
JavaScript converts the string to a number and then performs the comparison.
Example: 5 == "5" → true because "5" is converted to 5.

4. If one operand is a boolean:
JavaScript converts the boolean to a number (true to 1 and false to 0) and then performs the comparison.
Example: true == 1 → true because true is converted to 1.

5. If one operand is an object and the other is a primitive (number, string, etc.):
JavaScript attempts to convert the object to a primitive using the object’s .valueOf() or .toString() methods.
After converting the object to a primitive, JavaScript applies the comparison.
Example1: [1]=="1" ->true because [1] is converted to "1" .
Example2: [1] == 1 → true because [1] is converted to "1", which then converts to 1.

7. Special Case for NaN:
NaN is never equal to anything, including itself.
Example: NaN == NaN → false.
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

<details>
 <summary>Weird things of JavaScript</summary>
 <ul>
  
  *<li>The Boolean converstion of string which has only spaces is true and type conversion of  empty string is false.But if these both strings are converted into numbers then they both are converted to 0. For the empty string it is obvious but for the string with spaces it is a weird thing that why did it gets converted to 0 </li>*
  <li>Boolean of [] is true but number conversion of [] is 0.It is because first the [] will be converted into string "" and the number conversion of empty string and string with only spaces is 0.</li>
  <li>  If we do comparison of NaN with anyone then we will get false everytime.(EVEN IF WE DO COMPARISON OF NAN WITH NAN , WE WILL GET FALSE )</li>
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
<li><b>Reason</b> : Here as none of the operand is string so the + will do addition here and for this addition to take place it will make both the operands of same type i.e number type.Here,undefined will be converted into NaN and any computation with NaN yields in NaN.</li>
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
<li><b>Reason</b> : Any comparison of NaN results in false.</li>
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
<li><b>Reason</b> : The object gets converted to "[object Object]", and the array gets converted to "1,2,3".And after type conversion as anyone of the operand is in string format then concatenation will take place.</li>
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
<li><b>Reason</b> : JavaScript  tries .toString() on {}, which results in the string "[object Object]".and When JavaScript attempts to convert "[object Object]" to a number, it fails and results in NaN (Not a Number).And finally Any arithmetic operation involving NaN results in NaN.</li>
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
  lastName:undefined,
};
const { firstName="John",lastName="Chawla" } = person;
console.log(firstName,lastName);
```

<details>
<summary><b>View Answer</b></summary>
<ul>	
<li><b>Output</b> : Tushar,Chawla</li>
<li><b>Reason</b>  The `firstName` property in the `person` object has the value 'Tushar'. The default value "John" is ignored because it only applies when the property does not exist or is `undefined` and same reason for the lastName property.
</li>
</ul>
</details>

**[Scroll to Top](#Javascript-Output-Based-Question)**
