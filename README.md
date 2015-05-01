# Javascript Basics & Guidelines

## Table of contents

1. [Comments] (#comments)
1. [Types (Primitives)] (#datatypes)
1. [Arrays] (#arrays)
1. [Objects] (#objects)
1. [Strings] (#strings)
1. [Functions] (#functions)
1. [Variables] (#variables)
1. [Conditional Statements] (#conditional statements)
1. [Comparison Operators] (#comparison operators)
1. [Loops] (#loops)
1. [Prototypes] (#prototypes)


## comments

  - **comments**: In javascript there are 2 types of comments

    + `Single line comment`

    + `Multi line comment`
    

    ```javascript
    //this is a single line comment

    /*
      this is a multi line comment
    */
    ```
**[⬆ back to top](#table-of-contents)**

## datatypes

  - **Primitive data types**: 

    +  `number`

    +  `string`

    +  `boolean (true or false)`

    +  `undefined`

    +  `null`


    ```javascript
      var foo = 1; //number
      var bar = 'Hello World'; //string
    ```

  - Above primitive data type values are accessed directly without any reference. 

  - **Other datatypes**: such as object, array are accessed by its reference

    + `object`

    + `array`


    ```javascript
      var foo = [1, 'hello']; //array
      
      foo[0] = 1; //accessing array value by its reference
      
      var bar = {
        name: 'Hello World' 
      }; //object

      bar.name = 'Hello World'; //accessing object by its reference
    ```
**[⬆ back to top](#table-of-contents)**

## arrays

 - Array creation using literal syntax

    ```javascript
    //Bad
    var foo = New Array();

    //Good
    var foo = []; //array literal
    ```
  
  - Array starts at index 0

    ```javascript
    var bar = [1]; // array starts at index 0
    
    console.log(bar[0]); //print 1
    ```

  - Add a new item to an array

    ```javascript
    var bar = [1];
    bar.push(2); //adds 2 at the end of an array

    console.log(bar); //print [1, 2]
    ```

    - Add a new item at start of an array
    <br>

    ```javascript
    var bar = [1];
    bar.unshift(2); //adds 2 before 1

    console.log(bar); //print [2, 1]
    ```
  
    - Remove an item at the end of an array
	<br>

    ```javascript
    var bar = [2, 1, 2];
    bar.shift(2); //removes 2 from the start

    console.log(bar); //print [1, 2]
    ```

    - Remove an item at start of an array
	<br>

    ```javascript
    var bar = [2, 1, 2];
    bar.pop(2); //removes 2 from the end

    console.log(bar); //print [2, 1]
    ```

  - Get the length of an array

  ```javascript
    var bar = [1, 2, 'hello'];

    console.log(bar.length); //print 3
  ```
  
**[⬆ back to top](#table-of-contents)**

## objects

 - Object creation using literal syntax

  ```javascript
    //bad
    var obj = new Object();
    
    //good
    var obj = {}; //empty object literal
  ```

  - Accessing an object

  ```javascript
    var obj = {
      name: 'ABC',
      type: 'Alphabet',
      id: 123
    };

    console.log(obj.name); //print ABC

    console.log(obj['name']); //print ABC
  ```

  - Use better naming convension and don't use [reserved keywords](http://www.w3schools.com/js/js_reserved.asp) such as private, class etc.

  ```javascript
    //bad
    var obj = {
      class: 'car'
    };

    //good
    var obj = {
      type: 'car'
    };
  ```
**[⬆ back to top](#table-of-contents)**

## strings

  - Using single quote `''` for strings

  ```javascript
    //bad
    var bar = "Hello world";

    //good
    var bar = 'Hello world';
  ```  

  - Using `+` to concatenate strings

  ```javascript
    var bar = 'Hi I am ' + 'gokul';
  ```

**[⬆ back to top](#table-of-contents)**


## functions

  - Function declarations

  ```javascript
    function funz(name) {
      alert('My name is ' + name); //will alert my name is gokul
    }

    funz('gokul'); //call's the above function with argument

    var newFunz = new funz(); //creates an instance of the function funz
  ```

  - Function expressions

  ```javascript
    //anonymous function
    var funz = function() {
      alert('I am a function too');
    };

    funz();
    
    //Named function expression
    var namedFunz = function funz() {
      alert('I am a function too');
    };

    namedFunz();
  ```

  - Immediately invoked function express (IIFE)

    - below function is called automatically
    <br>

    ```javascript
    (function () {
      alert('I am a function which is invoked automatically');
    });
    ```

**[⬆ back to top](#table-of-contents)**

## variables

  - Variable creation

  ```javascript
  //bad
  foo = 1; 
  
  //good
  var foo = 1; //assigns number 1 to the variable foo
  ```

  - local and global variables in functions
  
  ```javascript
  //global
  var foo = 1; 

  alert(foo); //will alert 1

  function funz() {
    var bar = 10; //local variable
    console.log(bar); //print 10
    foo = 10; //changing the global variable value 1 to 10
  }

  alert(foo); //will alert 10

  funz(); //calling the function
  ```

**[⬆ back to top](#table-of-contents)**

## conditional statements

- If, Else if, Else Statement
  
  ```javascript
  var a = false;
  var b = true;

  //If the below condition is true, call alert()
  if (a) {
    alert('I am a if statement');
  }
  else if (b) {
    alert('I am else if statement'); //Will alert because b == true
  }
  else {
    alert('I am else statement');
  }
  ```  

**[⬆ back to top](#table-of-contents)**

## comparison operators

- Always use `===` instead of `==` and `!==` instead of `!=`

- Difference is that `===` and `!==` will also check the type of the variable, See below example


  ```javascript
  var foo = 1;
  var bar = '1';
  
  console.log(foo == 1); //True, because `==` will do automatic type conversion

  console.log(bar === 1); //False, because 1 === '1'

  console.log(bar === '1'); //True

  console.log(bar !== 1); //True , '1' is not equal value as well as type

  ```

## loops

 - for, for/in, while, do/while loop

  -- for loop

  ```javascript
  for (statement 1; statement 2; statement 3) {
    
  }

  //statement 1 - Executes before the loop
  //statement 2 - Condition to run the loop
  //statement 3 - Executes each time after the loop

  //See below for example

  for (var i = 0; i < 10; i++) {
    console.log(i); //Will print from 0 to 9
  }
  
  ```

  -- for/in loop to loop through an array or object

  ```javascript

  for (var x in array or object)  {
  
  }

  //Looping through an array
  var foo = [1, 2, 3, 4, 5];

  for (var i in foo) {
    console.log(foo[i]); //Will loop the array and prints 1 to 5
  }
  
  //Looping through an object
  var obj = [{ name : 'gokul'}, {name : 'krishh'}];

  for (var name in obj) { 

    //To check property belongs to object, not to prototype object
    //hasOwnProperty is only to check objects
    
    if (obj.hasOwnProperty(name)) {
      console.log(obj[name]); //Will print {name: "gokul"}, {name: "krishh"}
    }

  }

  ```  

  -- while loop


  ```javascript
  while (statement 1) {
    
  }

  //statement 1 - Condition to run the loop
  //See below for example

  var i = 0;

  while (i < 10) {
    i++; //Increment i
    console.log(i); //Will print from 1 to 10
  }
  
  ```

  -- do/while loop will execute once, before checking the condition in while


  ```javascript
  do {
    //Execute once before checking while condition
  } while(statement 1)

  //statement 1 - Condition to run the loop
  //See below for example

  var i = 0;

  do {
    console.log(i); //Will print from 0 to 10
    i++; //Increment i
  } while (i < 10) 
  
  ```

**[⬆ back to top](#table-of-contents)**

## prototypes

  - In javascript function, array, objects are considered as objects

  - All objects in js inherit, properties and methods from the prototype

  ```javascript
  function person(name, age) {
    this.name = name;
    this.age  = age;
    console.log(this.model);
  }
  
  person.prototype.model = 'Car'; //Addind model to prototype

  var newPerson = new person('Gokul', 23);

  ```

#### More contents are coming soon...

# Contribution

 If the contents above need to be improved or if you want to add more content to it. Feel free to fork and give me pull request.

 Thanks!!


## Author

[![Gokulakrishnan](https://avatars0.githubusercontent.com/u/2944237?v=3&s=72)](https://github.com/gokulkrishh)


License
----

MIT

