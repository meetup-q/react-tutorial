# JavaScript EcmaScript
> “Any application that can be written in JavaScript, will eventually be written in JavaScript.” – Jeff Atwood 

JavaScript 的歷史基本上就是 90 年代起的瀏覽大戰。

EcmaScript 是一個語言的 specification，而 javascript 則是依照 EcmaScript 的規範所實作出來的語言，所以 JavaScript 就是 EcmaScript，我們簡稱 ES。ES 每過一段時間就會更新，當我們會稱第五代為 ES5、第六代為 ES6。ES6 之後因為 javascript 的影響力越來越大所以 ECMA(Ecma International) 決定每年都會更新，例如我們會稱 2021 年發出的版本為 ES2021。

年年更新的 EcmaScript 絕對讓 javascript interpreter 的更新速度跟不上，但 developers 就是喜歡新的功能，所以有了 babel 這樣的工具出現，我們可以盡情地撰寫 ES6 以後的版本，然後在透過 babel 編譯成比較舊版的 ES。

# ES5 
ES5 又稱 ES2009，主要新增了 Array 與 Object 的 method，例如 map、reduce、keys。ES5 是重要的里程碑，從這一代開始 ES 變得更好寫了。

# ES6
ES6 又稱 ES2015，可以說是最重要，這一代新增的功能完全改變了 ES 的寫法，新增了 class、async await、arrow function、模組化的功能。也是自 2015 年起，ECMA 決定每年更新 EcmaScript，表示 JavaScript 越來越重要了。

# TypeScript
TypeScript 是由 Microsoft 所開發的語言，簡稱 TS，本質上還是 JavaScript，唯一的不同處如其名，要求變數不得改變其型別。因為 JavaScript 誕生之初的目標受眾是 non-programmer如網頁設計師或 Hobbist，必須讓這個語言好學好懂好寫，所以預言設計上不需先行宣告變數型態，然而這是有缺點的，大型程式或多人協作專案可能因為程式碼變數型別問題造成 bug，JavaScript 自行轉換變數的機制讓人困惑，TypeScript 的出現解決了這個問題。

# Babel
EcmaScript 每年更新但是 Browser 的支援進度跟不上，而 Developers 又是喜新厭舊的人群，該怎麼辦呢？雖然 interpreter 還未支援新的語法，但新的語法仍然可以被改寫成舊的語法，例如 arrow function 是 ES6 的產物，但若 brwser 不支援 arrow function 的話，我們可以將其改寫成原有的 function。我們需要一個 convertor 將比較新穎的 interpretor 還未支援的語法以舊的語法重構，這個 convertor 就是 babel。

因為幾乎所有 Browser 都對 ES5 全面支援了，所以我們會將語法轉換成 ES5。

# npm
npm 是 node.js 套件管理器（node.js package manager）由 npm inc. 維護。npm inc. 是一家營利公司，2020 年被 microsoft 收購，同年 npm 宣布移入 GitHub。[^Github 也為 microsoft 的子公司，此舉被解讀為增加 JavaScript 使用人數。]


# node.js
Ryan Dahl 在 2009 年發表了 node.js，一個基於 V8 engine 製作的 run time language，它的出現使得前後端都使用 javascript 得以成真。

注意 node.js 跟前端的 javascript 本質上是不一樣的語言。在 client-side 運行的  javascript 是遵行 EcmaScript 規範的語言，不同 Browser 因為直譯器不同的關係，有些許運行上的差異；而 node.js 的直譯器是 Chrome 的 V8 engine。

Developers 應該謹記著 JavaScript 與 node.js 兩著不同的事實，儘管在初淺的應用不會造成任何影像，在開發的深水區會是個問題。

# Deno.js
Ryan Dahl 在 node.js 十週年之際，列出了 node.js 的十大缺點，接著表示以 TypeScript 的  run time Deno.js 改進了這些缺點。目前 Deno.js 仍處於發展階段，是值得觀察的新工具。[^Deno 的名稱源自於 node 重新排列。]

# React.js
 
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

```
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

jQuery 就是典型的 Imperative 工具，為了達成一個功能，developer 必須用寫下每一個步驟。Imperative 的好處在於我們可以更掌握底層運作，壞處是 code 會變得繁瑣；declarative 的好處就是 code 更好寫，可讀性也會提高，壞處是相對的就是底層運作被掩蓋住了，遇到高效調教時比較麻煩。

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