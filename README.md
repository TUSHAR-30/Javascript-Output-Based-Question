# Javascript Output Based Question
```
hello world
ello
```

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

---
**1. What will be the output**
```
let arr = [1, 2, 3, 4, 5, -6, 7];
arr.length = 0;
console.log(arr);
```

	<details>
		<summary><b>View Answer</b></summary>
	<ul>	
		<li><b>Output</b> : [ ]</li>
		<li><b>Reason</b> : The length of the array has been set to 0, so the array becomes empty.</li>
	</ul>
	</details>

	**[Scroll to Top](#javascript-output-based-interview-questions)**
