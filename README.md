# Javascript basics and guidelines

This page also contains simple guidelines to follow, when you are writing Javascript.

## Table of contents

1. [Comments] (#comments)
1. [Types (Primitives)] (#datatypes)
1. [Arrays] (#arrays)
1. [Objects] (#objects)
1. [Strings] (#strings)
1. [Functions] (#functions)
1. [Variables] (#variables)
1. [Conditional Statements] (#conditional stmt)
1. [Loops] (#loops)
1. [Callbacks] (#callbacks)
1. [Prototypes] (#prototypes)
1. [Naming Convention] (#naming conventions)


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
    
    ```javascript
    var bar = [1];
    bar.unshift(2); //adds 2 before 1

    console.log(bar); //print [2, 1]
    ```
  
    - Remove an item at the end of an array
    ```javascript
    var bar = [2, 1, 2];
    bar.shift(2); //removes 2 from the start

    console.log(bar); //print [1, 2]
    ```

    - Remove an item at start of an array
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

# More contents are coming soon



License
----

MIT

