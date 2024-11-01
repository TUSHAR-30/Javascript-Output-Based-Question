# Javascript-Output-Based-Question
//if undefined tries to convert itself into number then it will converted into NaN(Not a number).


//As the comparison operator return true or false . If we do comparison of NaN with anyone then we will get false everytime.(EVEN IF WE DO COMPARISON OF NAN WITH NAN , WE WILL GET FALSE )


// if any of operand is object or array then they will be converted into primitive(number or string)


// arithmetic + operator
// if any of the operand is string then the + operator will concatenate both the operands.
// else the addition will be done and for this the operand will be first converted into numbers and then addition will take place.


//arithmetic - operator
// In JavaScript, when the subtraction operator - is used, the operands are converted to numbers before performing the subtraction


// Comparison > operator or Comparions < operator
// For > operator Both the operands will be converted into numbers in this case and then comparison of greater than or less than will take place


// Comparison == operator
// The == operator tries to make both the operands of same type if they are not of same type  i.e number type and then do compaison.
//But null and undefined are two operands which will never be converted into numbers in == operator.
//null==null , null==undefined , undefined == undefined (These are the true cases for null and undefined)


// Comparison === operator
// It does not do any type conversion and only give true if both the data type and value of operands is same.
// And there is no special case for null and undefined but it was there in == operator.
//null === null(true) undefined === undefined(true) null === undefined(false)








// Summary of Notes
// Undefined to Number:

// Correct: undefined converts to NaN when treated as a number.
// Comparing NaN:

// Correct: Any comparison with NaN results in false, including NaN === NaN, which is a unique case in JavaScript.
// Objects and Arrays to Primitive:

// Correct: Objects and arrays are converted to primitives (usually numbers or strings) when involved in operations.
// Addition (+) Operator:

// Correct: If either operand is a string, JavaScript concatenates the operands. Otherwise, it converts them to numbers before performing addition.
// Subtraction (-) Operator:

// Correct: Both operands are converted to numbers before subtraction is performed.
// Comparison Operators (> and <):

// Correct: Both operands are converted to numbers before comparison. If one or both cannot be converted to a number, the result may be NaN.
// Equality (==) Operator:

// Correct: The == operator performs type coercion to make operands the same type for comparison. Notably, null and undefined are special cases that do not convert to numbers and can equal each other.
// Strict Equality (===) Operator:

// Correct: The === operator checks both value and type without any type conversion. Hence, it treats null and undefined distinctly.
