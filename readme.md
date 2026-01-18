# JavaScript

## assignments

1.  Explain the scope in JavaScript.

    - In JavaScript, **scope** determines the accessibility of variables, functions, and objects in different parts of the code. There are three main types of scope:


    1. **Global Scope** – Variables declared outside any function are accessible anywhere in the script.
    2. **Function Scope** – Variables declared inside a function are accessible only within that function.
    3. **Block Scope** (introduced with `let` and `const`) – Variables declared inside `{}` (like loops or `if` blocks) are only accessible within that block.

2.  What is a callback?

    - A **callback** is a function that is passed as an argument to another function and then invoked inside the outer function to complete some task.

    ```javascript
    function outerFunction(callback) {
      // do something
      callback();
    }
    outerFunction(function () {
      // do something
    });
    ```

3.  Explain context in JavaScript?

    - In JavaScript, **context** refers to the **environment** in which a function is executed. It determines the value of `this` inside the function.

    ***

    1. **Global Context** – `this` refers to the global object in the browser (window in Node.js).
    2. **Execution Context** – `this` refers to the **current** object in which the function is executed.

4.  What is hoisting in JavaScript?

    - hoisting -> it is the declaration of variables functions and classes are taken to the top of the scope before the execution of code this behavior of javascript is known as hoisting.

    ```javascript
    var a = 10;
    console.log(a);
    var a; // 10
    ```

5.  Explain lexical scope?

    - lexical environment -> the area where the variables and their values are accessible during the execution of the code.

    ```javascript
    let FirstName = "Sri";
    let SecondFunction = () => {
      console.log(FirstName);
      let SecondName = "Ram";
      let ThirdFunction = () => {
        console.log(FirstName + SecondName);
      };
      ThirdFunction();
    };
    SecondFunction();
    ```

6.  What is scope chaining?

    - scope chaining -> unidirectional flow of scope. the scope of a variable is determined by the nearest enclosing scope.

7.  Explain coercion?

    - coercion -> is the automatic conversion of one data type to another data type.

    ```javascript
    let a = 10;
    let b = "20";
    console.log(a + b); // 1020
    console.log(a + parseInt(b)); // 30
    console.log(a + Number(b)); // 30
    ```

8.  Explain closure?

    - closure -> is the combination of a function and its lexical environment within which the function declared.

    ```javascript
    let FirstFunction = () => {
      let FirstName = "sree";
      let SecondFunction = () => {
        console.log(FirstName);
        let SecondName = "ram";
        let ThirdFunction = () => {
          console.log(FirstName + SecondName);
        };
        ThirdFunction();
      };
      SecondFunction();
    };
    FirstFunction();
    ```

9.  What is the difference between undefined and not defined in JavaScript?

    - undefined -> value of a variable that is not initialized, or the value of a variable that is declared but not assigned a value.

    - not defined -> value of a variable that is not initialized, or the value of a variable that is declared but not assigned a value.

10. Explain spread and rest operator?

    - spread operator -> allows an iterable to be expanded in places where zero or more arguments are expected.

    ```javascript
    const Arr = [1, 2, 3];
    const NewArr = [...arr, "four", "five"];
    console.log(NewArr); // 1 2 3 'four' 'five'
    ```

    - rest operator -> allows a function to accept a variable number of arguments.

    ```javascript
    let add = (a, b, c, ...rest) => {
      console.log(rest); // [6, 8, 10]
      console.log(a); // 2
      console.log(b); // 4
    };
    add(2, 4, 6, 8, 10);
    ```

11. Explain ‘this’ keyword in Javascript?

    - In JavaScript, the `this` keyword refers to the current execution context. It can be used to access the current object, the global object, or the window object in a browser environment.

    ```javascript
    let user = {
      Name: "sreeram",
      Age: 21,
      Address: "alaparambil ram nivas manissery PO",
      Pin: 679521,
      PhoneNo: 8111852220,
      details: function () {
        console.log(this.Name);
        console.log(this.Age);
        console.log(this.Address);
        console.log(this.Pin);
        console.log(this.PhoneNo);
      },
    };
    console.log(user);
    user.details();
    ```
