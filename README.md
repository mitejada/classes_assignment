# Class Exercises

<!-- 1.
  * Create a Human class that takes in a name and age.
  * Add the function `ageOneYear` that ages the human.
  * Add the function `eating`, that logs "mmm, mmm, mmm, I'm love'n it".
  * Create an instance of the Human class.
    * console log your humans age
    * call ageOneYear on your human
    * console log their age again.
    * call eating on your human.




<!-- 2.
Write a class Vector that represents a vector in two-dimensional space.
It takes two number arguments: `x` and `y` parameters, which it should be saved to properties of the same name.

Give the Vector two methods, `plus` and `minus`, that take another vector as an argument and
returns a new vector that has the sum or difference of the two vectors’ (the one in `this` and the parameter) x and y values.

Add a method `getLength` to the prototype that computes the length of the vector ;
that is, the distance of the point (x, y) from the origin (0, 0).(a^2 + b^2 = c^2)

```js
var v1 = new Vector(1, 2)
var v2 = new Vector(2, 3)
console.log(v1.plus(v2));
// => Vector {x: 3, y: 5}
console.log(v1.minus(v2));
// => Vector {x: -1, y: -1}

var v3 = new Vector(3, 4)
console.log(v3.getLength());
// => 5
``` -->


1.
class Human {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  ageOneYear() {
    this.age++
    return `You are now ${this.age} years old`;
  }

  eating() {
    return `mmm, mmm, mmm, I'm love'n it`
  }
}

let newHu = new Human ('Michell', '25')
console.log(newHu.age);
console.log(newHu.ageOneYear())
console.log(newHu.eating())


2.
class Vector {
  constructor(x, y) {
    this.x = x;
    this.y = y;
  }

  plus(vec) {
    let addition = this.x + vec.x;
    let addition2 = this.y + vec.y;
    return `x: ${addition} , y: ${addition2}`;
  }

  minus(vec) {
    let subtraction = this.y - vec.y;
    let subtraction2 = this.y - vec.y
    return `x: ${subtraction} , y: ${subtraction2}`;
  }

  getLength (nums) {
    let length = Math.hypot(this.x,this.y)
    return length;
  }
}


let v1 = new Vector (1, 2)
let v2 = new Vector (2, 3)
let v3 = new Vector (3, 4)

console.log(v1.plus(v2))
console.log(v1.minus(v2))
console.log(v3.getLength())
