# JavaScript

這裡是基本的 JavaScript 語法，目標讀者是沒有寫過 JavaScript 的新進前端開發者。

# 基本語法

JavaScript 的基本語法

比起 Java 、 C 語言來說，JavaScript 跟 Python 一類的語言一樣非常好上手，
它的靈活、易寫與跨平台的特性，被當作是最適合成為每個人的第一個語言。
以下是 W3School 的教學。

[W3School](https://www.w3schools.com/js/default.asp)

我們並不會教學所有語法，我們只會提及一些必須事先知道的語法，
當我們之後遇到比較陌生的語法會另作講解。

基本語法：

以下的語法都以 ES6 為主。

### declare variable

ES6 之前，我們在定義變數的指令是 var。

在 ES6 之後提供了 const & let。
const 表示被宣告的變數是常數，不能再被更改；
let 表示被宣告的變數是變數，可以被再賦值。
什麼時候該用 const 什麼時候該用 let？
程式設計中最困擾人的工作就是變數命名，所以我們不要在在這個問題上困擾自己，
簡化之為優先使用 const，當有需要改變變數時再使用 let。

```javascript
const name = 'handsome boy'

name = 'handsome man'
// throw an error. boy will never become a man

let age = 26

age++
// age is 27 
```

### function

ES6 提供 arrow function 讓我們定義函數，這種寫法比原本的寫法還要簡潔。

```javascript
// pre ES6
function greeting(){
  console.log(`Hi, there. My name is ${name}`)
}
// 匿名函數
function(){
  console.log(`I don't have a name.'`)
}
```

```javascript
// arrow function
const greeting = () => { 
    console.log(`Hi, there. My name is ${name}`) 
  }
  
() => {
  console.log(`I am much more short.`)
}
```

### ES6 class

```javascript
class Square {
  constructor (sideLength){
    this.width = sideLength
    this.height = sideLength
  }
  get area() {
    return this.width * this.height
  }
  
  set area(value) {
    this.widht = Math.sqrt(value)
    this.height = Math.sqrt(value)
  }
}

```

```javascript
class Foo {
    constructor(prop) {
        this.prop = prop;
    }
    static staticMethod() {
        return 'classy';
    }
    prototypeMethod() {
        return 'prototypical';
    }
}
const foo = new Foo(123);
```

[js class explaination](https://exploringjs.com/es6/ch_classes.html)

constructor is a special method representing this class.

``` js
Foo === Foo.prototype.constructor 
// => true
```


# 參考資料
1. You Don't Know JavaScript full series. 
2. [js class explaination](https://exploringjs.com/es6/ch_classes.html)