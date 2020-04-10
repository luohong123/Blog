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

18. 以下输出: Hmm.. You don't have an age I guess
```javascript
function checkAge(data) {
    if (data === {
            age: 18
        }) {
        console.log('You are an adult!')
    } else if (data == {
            age: 18
        }) {
        console.log('You are still an adult.')
    } else {
        console.log(`Hmm.. You don't have an age I guess`)
    }
}
checkAge({age:18})
```
打印预览:

19. 以下输出: object
```javscript
function getAge(...args) {
    console.log(typeof args)
}
getAge(21)
```
打印预览:

20. 以下输出: ReferenceError: age is not defined
```javascript
function getAge() {
    'use strict'
    age = 21
    console.log(age)
}
getAge()
```
打印预览:

21. 以下输出: 105
```javascript
const sum = eval('10*10+5')
console.log(sum)
```
打印预览:

22. sessionStorage 储存的数据可以保存多长时间？
当用户关闭标签页时

23. 以下输出: 23
```javascript
var num = 8
var num = 10
console.log(num)
```
打印预览:

24. 以下输出: true true false true
```javascript
const obj = {
    1: 'a',
    2: 'b',
    3: 'c'
}
const set = new Set([1, 2, 3, 4, 5])
console.log(obj.hasOwnProperty('1'))
console.log(obj.hasOwnProperty(1))
console.log(set.has('1'))
console.log(set.has(1))
```
打印预览:

25. 以下输出: { a: 'three', b: 'two' }
```javascript
const obj = { a: 'one', b: 'two', a: 'three' }
console.log(obj)
```
打印预览:


26. JavaScript 全局执行上下文为你做了两件事：全局对象和 this 关键字(^_^)

27. 以下输出: 1 2 4
```javascript
for (let i = 1; i < 5; i++) {
    if (i === 3) continue
    console.log(i)
}
```
打印预览:

28. 以下输出: Just give Lydia pizza already!
```javascript
String.prototype.giveLydiaPizza = () => {
    return 'Just give Lydia pizza already!'
}
const name = 'Lydia'
console.log(name.giveLydiaPizza())
```
打印预览:

29. 以下输出 456
```javascript

const a = {}
const b = { key: 'b' }
const c = { key: 'c' }
a[b] = 123
a[c] = 456
console.log(a[b])
```
打印预览:

30. 以下输出: First Third Second
```javasript
const foo = () => console.log('First')
const bar = () => setTimeout(() => console.log('Second'))
const baz = () => console.log('Third')
bar()
foo()
baz()
```
打印预览:

31. 导致事件的最深嵌套的元素是事件的 target,可以通过 event.stopPropagation 来停止冒泡

32. 在事件传播期间，有三个阶段：捕获、目标和冒泡。默认情况下，事件处理程序在冒泡阶段执行。

33. 
