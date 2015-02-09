# Javascript basics and guidelines

This page also contains simple guidelines to follow, when you are writing Javascript.

## Table of contents

1. [Comments] (#comments)
1. [Types (Primitives)] (#types)
1. [Objects] (#objects)
1. [Arrays] (#arrays)
1. [Strings] (#strings)
1. [Functions] (#functions)
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

## types

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

## objects

  - Do's and dont's in object

    ```javascript
    //bad and old way
    var item = new Object();

    //good
    var item = {}; //object literal
    ```  
  
  - Use better naming convension and don't use [reserved keywords](http://www.w3schools.com/js/js_reserved.asp) such as private, class etc.

    ```javascript
    //bad
    var item = {
      'klass': 'Audi'
    };
    
    //good
    var item = {
      'type': 'Audi'
    };
    ```  
  **[⬆ back to top](#table-of-contents)**

## arrays

 - Do's & dont's in array 

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


# More contents are coming soon



License
----

MIT

