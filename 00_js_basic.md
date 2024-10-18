# Java Script:


### Vanilla JS :

    Javascript without any libraries

### Jquery: 
    It is popular library of JS. simplies HTML manupulation, event handling.

## what we can do with JS
1.  Front end
2.  Back-end
3.  Mobile
4.  Desktop

### Front end JS
1.  React
2.  Angular
3.  Vue

### Backend JS



### JS for Mobile
1. React Native
2. Native script

### JS for Desktop
1. slack
2. electron

### Javascript features
1. JS is an interpreted language
    . Executed without compiling
    . no coversion of code, not to bytecode, not to machine code

2. JS is dynamic typed and weakly typed
Dynamic type
let a = 10;

static type
int a = 10;

3. JS has support for OOP
4. JS is single-thread


### Pros and cons of JS

#### cons
1. problem with the browser suppot
2. security concern


### Javascript dialects
1. TS
2. coffeescript
3.  elm
4.  dart

### how to declare a variable
    let a =10;
    var b = 10;

#### difference between let and var

    console.log('let vs var');
    
    function foo1(){
    
      if(true){
        c = 1; //global
        var a = 100;  //function scope
        let b = 200;  //block scope
      }
      console.log(a);
    }



### Javascript Datatype
1. Number
2. boolean
3. string
4. object
5. function
6. undefined
7. bigints
8. symbol


#### number
    let natural = 10;
    let decimal = 10.1;
    let hex = 0xa;
    let binary = 0b1010;
    let octal = 0o52;
    let fivLakhs = 5e5;
    console.log(natural, decimal, hex, binary, octal, fivLakhs);
    console.log(typeof natural, typeof decimal, typeof hex, typeof binary, typeof octal, typeof fivLakhs);

    //two special value of number Nan and Infinity
    let a = 10 * 'hello';
    console.log(a, typeof a);

    let b = 10 /0;
    console.log(b, typeof b);

#### string
    let sigleQuoteString = 'single quote';
    let doubleQuoteString = "double quote";
    let backTickString = `back tick `; 


#### boolean
    true and false are the two value of boolean
    falsely value
        let b = false;
        b = 0;
        b = "";  //'', ``
        b= null;
        b = undefined;
        b = NaN;
        b = 0n;

        if (b) {
        console.log("true");
        } else {
        console.log(b, "false");
        }

#### object type
    //object
    let person = {
    name :'jack',
    age : 20,
    nationality : 'Indian'
    };

    console.log(person);
    console.log(typeof person);

    //access the properties
    person.name = 'Ajay';  //dot notation
    person['age'] = 25;    //bracket notation

    console.log(person);

    let math = {0 : 'zero', '+':'addition','-':'subtraction','*':'multiplication','/':'division'};
    console.log(math);
    //console.log(math.0); //cannot access above propterties with dot notation
    console.log(math['0']);


#### function
    //function
    function add(a, b) {
    let c = a + b;
    return c;
    }

    console.log(add);
    console.log(typeof add);

    let add1 = function (a, b) {
    let c = a + b;
    return c;
    };

    console.log(add1, typeof add1);

    let add2 = (a, b) => a + b;
    console.log(add2, typeof add2);

    console.log(add(100, 200));
    console.log(add1(100, 200));
    console.log(add2(100, 200));

--------------------------------------------------
    console.log(add(100, 200));  //this will work
    console.log(add1(100, 200));  //this will not work

    function add(a, b) {
    let c = a + b;
    return c;
    }


    let add1 = function (a, b) {
    let c = a + b;
    return c;
    };

#### undefined
    let a;
    let person = {name:'jack'};
    console.log(a, typeof a); // undefined, 'undefined'
    console.log(person.age);  //undefined
    let person1 = null;
    console.log(person1, typeof person1); //null object
    console.log(typeof null);  // object

#### bigints
    let a = 123456789123456789n;
    console.log(a, typeof a);

#### symbol
    symbol are used for ensuring uniquness
    let a = Symbol(10);
    let b = Symbol(10);
    console.log(a, typeof a);
    console.log(b, typeof b);
    console.log(a == b);


-----------------------------------------------------------------------------------
#### important features
##### equality
 1. ==  check equality of value
 2. === check equality of value and type

    let a = 10;
    let b = '10';
    console.log(a === Number(b));
    console.log(typeof a, typeof Number(b));

##### arrays
    Arrays are objects
    let arr = [1, 2, 3, 4];
    console.log(arr, typeof arr);  //[ 1, 2, 3, 4 ] object

    arr[2] = 100;
    console.log(arr); //[ 1, 2, 100, 4 ]

    //built in method
    arr.push(10);
    console.log(arr); //[ 1, 2, 100, 4 , 10]

    let x = arr.pop();
    console.log(x, arr);  //x= 10,   arr= [ 1, 2, 100, 4 ]

    console.log(arr.indexOf(1000));  //-1



    let barr = arr.filter(function (item) {
    return item % 2 === 0;
    });

    let carr = arr.filter((x) => x % 2 === 0);
    let darr = carr.map(x => x * x);

    console.log(darr);


###### splice function

    array.splice(
        startingIndex,
        removeHowManyElement,
        ... element to be added
    );

    array.splice(2,3,4,5);
    starting index = 2
    NumberOfElementTobeRemoved =3
    elementTobeAdded =4,5


##### spread operator
    . combine the objects and array
    . passing function argument to the function


    let person = {name: 'jack', age:22};
    let emp = {id:101, salary:2000};

    let empAsPerson = {...emp, ...person};
    console.log(empAsPerson);


    let arr = [1,2,3];
    let barr = [10,20,30];
    let carr = [...arr, 111, ...barr];
    console.log(carr);

    function add(num1, num2,num3){
        let rs =  num1 + num2 + num3;
        console.log('sum= '+rs);
    }

    add(arr[0], arr[1], arr[2]);
    add(...arr);

##### Object Destructuring






