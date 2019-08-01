1. 以下输出: undefined ReferenceError
```javascript
function sayHi() {
    console.log(name)
    console.log(age)
    var name = 'Lydia'
    let age = 21
}
sayHi()
```
打印预览:

2. 以下输出: 3 3 3 和 0 1 2
```javascript
for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1)
}

for (let i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1)
}
```
打印预览:

3. 以下输出: 20 和 NaN
```javascript
const shape = {
  radius: 10,
  diameter() {
    return this.radius * 2
  },
  perimeter: () => 2 * Math.PI * this.radius
}

console.log(shape.diameter())
console.log(shape.perimeter())
```
打印预览:

4. 以下输出: 1 和 false
```javascript
console.log(+true)
console.log(!"Lydia")
```
打印预览:

5. 以下输出: TypeError: Cannot read property 'size' of undefined
```javascript
const bird = {
    size: 'small'
}

const mouse = {
    name: 'Mickey',
    small: true
}
console.log(mouse.bird.size)
```
打印预览: 

6. 以下输出: Hello
```javascript
let c = { greeting: 'Hey!' }
let d
d = c
c.greeting = 'Hello'
console.log(d.greeting)
```
打印预览:

7. 以下输出: true false false
```javascript
let a = 3
let b = new Number(3)
let c = 3
console.log(a == b)
console.log(a === b)
console.log(b === c)
```
打印预览:

8. 以下输出: TypeError: freddie.colorChange is not a function
```javascript
class Chameleon {
    static colorChange(newColor) {
        this.newColor = newColor
        return this.newColor
    }
    constructor({
        newColor = 'green'
    } = {}) {
        this.newColor = newColor
    }
}
const freddie = new Chameleon({
    newColor: 'purple'
})
console.log(freddie.colorChange('orange'))
```
打印预览:

9. 以下输出: {}
```javascript
let greeting
greetign = {}
console.log(greetign)
```
打印预览:

10. 以下输出: 没有输出，正常运行
```javascript
function bark(){
    console.log('Woof!')
}
bark.animal='dog'
```
打印预览: 

11. 以下输出: TypeError: member.getFullName is not a function
```javascript
function Person(firstName, lastName) {
    this.firstName = firstName;
    this.lastName = lastName;
  }
  
  const member = new Person("Lydia", "Hallie");
  Person.getFullName = function () {
    return `${this.firstName} ${this.lastName}`;
}
  
console.log(member.getFullName());
```
打印预览:

12. 以下输出: Person { firstName: 'Lydia', lastName: 'Hallie' } 和 undefined
```javascript
function Person(firstName, lastName) {
    this.firstName = firstName
    this.lastName = lastName
  }
  
const lydia = new Person('Lydia', 'Hallie')
const sarah = Person('Sarah', 'Smith')
console.log(lydia)
console.log(sarah)
```
打印预览:

13. 事件传播的三个阶段是什么？
捕获(Capturing)=》目标(Target)=》冒泡(Bubbling)

14. 所有对象都有原型(❌)

15. 以下输出: '12'
```javascript
function sum(a, b) {
    return a + b
}
console.log(sum(1, '2'))
```
打印预览:

16. 以下输出: 0 2 2
```javascript
let number = 0;
console.log(number++)
console.log(++number)
console.log(number)
```
打印预览:

17. 以下输出: [ '', ' is ', ' years old' ] 'Lydia' 21
```javascript
function getPersonInfo(one,two,three){
    console.log(one)
    console.log(two)
    console.log(three)
}
const person = 'Lydia'
const age=21
getPersonInfo`${person} is ${age} years old`
```
打印预览:
