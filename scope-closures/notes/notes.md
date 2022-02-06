steps involved

1. tokeninzing/lexing - breaks expression into tokens
2. parsing `a AST abstract syntax tree is formed` - it does hoisting, find syntax errors and some early errors.
3. executing - executes the AST - converting AST into machine level instructions
4. machine understand these instructions, schedule them on CPU as per the scheduling strategy like round robin

code -> js engine tokenize -> js engine parsing -> js engine understanding the AST and converting it 
into byte code -> instructions goes to the CPU  

memory allocation - it is done by the underlying processor
**JS engine converts the code into machine language that can be processed by the CPU**

### targets
-- a value is assigned to a target

```js

var name = "yati" 
// var name is declaration handled at compiled time only
// name="yati" is assignment, done at execution time

```

```js
function getStudentName(studentID) {} // function declaration doen at compile time
```

```js
var getStudentName = function(studentID) {} /* function is a special case, assignment is 
also done at compile time and it is called function hoisting
*/
```

**scopes are identified during compilation and are created during runtime**