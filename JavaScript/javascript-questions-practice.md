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

