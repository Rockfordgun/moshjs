# Notes on Javascript

## Functions

```javascript 

function greet(name) {
    console.log("Hello, " + name + "!");
}

greet ("Anton")

```

## Objects

**Iterate/call inside an object**
```javascript

const adress = {
    street: 'Rue de la paix',
    city: 'Paris',
    zipCode: '75000'
}

function showAdress(adress) {
    for (let key in adress)
        console.log(key, adress[key]);
}

console.log(adress.street);

```

**Copy/Clone an Object**
```javascript

const circle = {
    radius: 1,
    draw() {
        console.log('draw');
    }
};

//spread operator ...
const circle2 = {...circle};

console.log(circle2);

```

**OOP**
```javascript

//NB COnstructor function always start with a caps 'Circle'
function Circle(radius) {
    this.radius = radius;
    this.draw = function() {
        console.log('draw');
    }
}

const circle = new Circle(1);

const circle2 = new Circle(2);

```

## Arrays

**How to add elements**
```javascript

const numbers = [1, 2, 3, 4, 5];

//End 'push'
numbers.push(6, 7, 8, 9, 10);
// console.log(numbers);
//msg 'Array(10) [ 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 ]

//Start 'unshift'
numbers.unshift(-2, -1, 0);
// console.log(numbers);
//msg Array(13) [ -2, -1, 0, 1, 2, 3, 4, 5, 6, 7, … ]

//Middle 'splice'
numbers.splice(5, 0, 1.1, 1.2, 1.3);
// console.log(numbers);
//msg Array(16) [ -2, -1, 0, 1, 2, 1.1, 1.2, 1.3, 3, 4, … ]

```

**Finding Primitives/Reference Types**
```javascript

// //Primitive Data Types
const numbers = [1, 2, 3, 4, 5];


console.log(numbers.indexOf(1)); // 0

//Reference Data Types
const courses = [
    {id: 1, name: 'a'},
    {id: 2, name: 'b'},
];

const course = courses.find(function(course) {
    return course.name === 'a';
});

console.log(course); 
// {id: 1, name: 'a'} 
// if u cant find a course.name 'undefined'

```
**Arrow Function**
```javascript

const courses = [
    {id: 1, name: 'a'},
    {id: 2, name: 'b'},
];

const course = courses.find (course => course.name === 'a');

console.log(course); // {id: 1, name: 'a'}

```
**Removing Elements**

```javascript

const numbers = [1, 2, 3, 4, 5];

//Begining
const first = numbers.shift();
console.log(numbers); // [2, 3, 4, 5]

//Middle
const middle = numbers.splice(2, 1);
console.log(numbers); // [2, 3, 5]

//End
const last = numbers.pop();
console.log(numbers); // [1, 2, 3, 4]

```
**Combine/Remove from Arrays**

```javascript

const first = [1, 2, 3, 4, 5];
const second = [6, 7, 8, 9, 10];

//Combine two arrays
const first = [1, 2, 3, 4, 5];
const second = [6, 7, 8, 9, 10];

//use Spread Operator
const combined = [...first, ...second];

//Remove elements from an array
const slice = combined.slice(2, 4);
console.log(slice); // [3, 4]

```
**Iterate through Array**

```javascript

const numbers = [1, 2, 3, 4, 5];
numbers.forEach((number) => console.log(number));     // 1 2 3 4 5

```

**Sorting Arrays**
```javascript
//Sorting Array
const numbers = [5, 3, 2, 4, 1];

numbers.sort();
console.log(numbers);  // [1, 2, 3, 4, 5]

//Reverse Order
const numbers = [5, 4, 3, 2, 1];

numbers.reverse();
console.log(numbers); // [1, 2, 3, 4, 5]

//Filter a Array
const numbers = [1, 2, 3, 4, 5];

const filtered = numbers.filter((n) => n > 3);
console.log(filtered); // [4, 5]

```
**Map an array**

```javascript

//Mapping
const numbers = [1, 2, 3, 4, 5];

const items = numbers.map(n => '<li>' + n + '</li>');
const html = '<ul>' + items.join('') + '</ul>';

console.log(html); // <ul><li>1</li><li>2</li><li>3</li><li>4</li><li>5</li></ul>

//Chaining Method

const numbers = [1, -1, 2, 3, 4, 5];

const items = numbers.filter(n => n >= 0)
.map(n => ({ value: n }));

console.log(items);


```

**Calculate the full value of an array**

```javascript

//Reduce Method calculate the sum of all the numbers in an array

const numbers = [1, 2, 3, 4, 5];

const sum = numbers.reduce((accumulator, currentValue) => {
  return accumulator + currentValue;
}, 0);

console.log(sum);

```

**How to access an array**

```javascript



```

**How to access an array**

```javascript



```

**How to access an array**

```javascript



```

## License

Mention the license under which your project is released.

## Contact

Provide contact information for users to reach out to you.


```javascript
function helloWorld() {
    console.log("Hello, world!");
}