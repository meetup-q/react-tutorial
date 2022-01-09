# EcmaScript
EcmaScript 是一個語言的 specification，而 javascript 則是依照 EcmaScript 的規範所實作出來的語言，所以 JavaScript 就是 EcmaScript，我們簡稱 ES。ES 每過一段時間就會更新，當我們會稱第五代為 ES5、第六代為 ES6。ES6 之後因為 javascript 的影響力越來越大所以 ECMA(Ecma International) 決定每年都會更新，例如我們會稱 2021 年發出的版本為 ES2021。

年年更新的 EcmaScript 絕對讓 javascript interpreter 的更新速度跟不上，但 developers 就是喜歡新的功能，所以有了 babel 這樣的工具出現，我們可以盡情地撰寫 ES6 以後的版本，然後在透過 babel 編譯成比較舊版的 ES。

# REACT TUTORIAL

Ryan Dahl 在 2009 年發表了 node.js，一個基於 V8 engine 製作的 run time language，它的出現使得前後端都使用 javascript 得以成真。

注意 node.js 跟前端的 javascript 本質上是不一樣的語言。在 client-side 運行的  javascript 是遵行 EcmaScript 規範的語言，不同 Browser 因為直譯器不同的關係，有些許運行上的差異；而 node.js 的直譯器是 Chrome 的 V8 engine。

npm 是 node.js 套件管理器（node.js package manager）由 npm inc. 維護。npm inc. 是一家營利公司，2020 年被 microsoft 收購。
 
react.js 是 facebook 在 2013 年發表的前端框架，facebook 的前端就是用 react.js 構成。跟據 stack overflow 與 GitHub 調查，react.js 是世界上最活躍的前端框架。

1. Declarative
2. State and props
3. Single Page Application
4. Client Side Rendering
5. one way data flow
6. component lifecycle
7. virtual dom
8. jsx

使用下方 code block 的 npm 指令創建一個 react project。指令中的 npx 是 npm 的一項指令，它可以協助下載所有 dependencies；myapp 是專案名稱。成功創造 react 專案之後在 myapp 之內執行 `npm start` 就可以在開發環境運行 react。
```
npx create-react-app myapp
```

當我們的專案需要更多套件的時候必須在專案資料夾下執行 `npm install package`，套件會被下載到專案資料夾內，並且記錄在 package.json 裡面。每個專案的 dependencies 都會被下載到自己的 node_modules 資料夾裡面，並不會污染到 global environment。

React 是 declarative 的工具，意思是我們只要告訴它結果，中間的過程它會自己想辦法。如下面這個例子，這是一個紀錄與顯示 button 被點擊的次數的 component，點擊 button 之後他就會更新 state count 並且重新 render component 以顯示新的數字。

```javascript
const Counter = () => {
  const [count, setCount] = useState(0)
  return(
    <div>
	  <button onClick={() => {setCount(count++)}}></button>
	  <div>The button has been hit {count} times</div>
    </div>
  )
}
```

jQuery 就是典型的 Imperative 工具，為了達成一個功能，developer 必須用寫下每一個步驟。Imperative 的好處在於我們可以更掌握底層運作，壞處是 code 會變得繁瑣；declarative 的好處就是 code 更好寫，可讀性也會提高，壞處是相對的就是底層運作被掩蓋住了，遇到高效調教時需要打開 black box。

react.js 在更新 dom 的時候不會為了小小的變動而更新整個 dom，這一切都要歸功於它的一項機制，virtual dom。virtual dom 會比較變更前後的 dom 找出需要被變更的地方再行變更，而不是整個 dom 更新，所以比較有效率。

jsx 是一個 mind blowing 的工具，我們可以把做好的 component 當作 html tag 一樣寫在 jsx 裡，這樣的寫法實踐了樂高式的設計，所有的 react compoent 都可以被當作樂高玩具一樣隨插隨用。
```
render(){
  return(
    <div>
      <Component1 />
      <Component2 name="foo" startPoints=10>
	    <p>lorem ipsum</p>
      <Component2>
    </div>
  )
}
```

one way data flow 是 react 的運作機制，components 的資料只能往 children nodes 傳下去，不能逆流而上。這個機制是為了確保資料更新不混亂。這個機制的缺點是資料交換很麻煩，所以出現了 state 儲存中心的工具 redux。

component lifecycle 是 component 的生命週期，developer 可以依照需求在 component 的某個生命週期執行對應的指令，lifecycle 的主要分類如下：
1. 
2. componentDidMount()
3. componentWillMount()

lifecycle 並非 react 創的特色，html5 的 createElement 也有類似的功能，我們在學習 framework 之餘也應該學習 plain html & javascript。

# React project 實作

接著我們會進行一個 react project。