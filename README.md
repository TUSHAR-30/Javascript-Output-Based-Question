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
