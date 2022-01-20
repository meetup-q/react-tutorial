# [Tutorial 1: JavaScript](./README.md)
> “Any application that can be written in JavaScript, will eventually be written in JavaScript.” – Jeff Atwood 

- [Tutorial 1: JavaScript](#tutorial-1-javascript)
- [JavaScript 的歷史](#javascript-的歷史)
  - [EcmaScript & JavaScript](#ecmascript--javascript)
  - [ECMA (European Computer Manufacturers Association)](#ecma-european-computer-manufacturers-association)
  - [ES5](#es5)
  - [ES6](#es6)
- [TypeScript](#typescript)
- [Babel](#babel)
- [node.js](#nodejs)
- [Deno.js](#denojs)
- [npm](#npm)
- [React.js](#reactjs)
  - [React.js features:](#reactjs-features)
    - [Single Page Application](#single-page-application)
    - [Virtual DOM](#virtual-dom)
    - [JSX](#jsx)

# JavaScript 的歷史

## EcmaScript & JavaScript

1995 年 12 月，Brendan Eich 在 Netscape 負責設計出應用於瀏覽器的語言，這個語言的名稱從 Mocha 輾轉到 LiveScript 最後在與 Sun Microsystems 聯合發表時公布為 JavaScript。在 1997 年 6 月 Netscape 向 ECMA 提交了 JavaScript 的規格書，在經由審定組織 TC-39 的審定後 ECMA 公告了 ECMA-262，也就是 ES1。以上就是 JavScript 的起源歷史，從中我們可以了解到 JavaScript 就是 EcamScript，前者是語言本身，後者是規格。

ECMA 每過一段時間就會更新 ES，而我們會稱第五代為 ES5、第六代為 ES6。在 ES6 之後因為 JavaScript 的影響力越來越大所以 ECMA 決定每年都會更新 ES，所以我們就以年份替換代數，例如我們會稱 2021 年發出的版本為 ES2021。

## ECMA (European Computer Manufacturers Association)
ECMA 原本是歐洲電腦製造協會的縮寫，但是 ECMA 的影響力日漸巨大，遂放棄原本的全稱，以簡寫表示這個組織，稱作 ECMA International。

## ES5 
ES5 又稱 ES2009，主要新增了 Array 與 Object 的 method，例如 map、reduce、keys。ES5 是重要的里程碑，從這一代開始 ES 變得更好寫了，2009 年至今也超過十年了，發展時間相當長，幾乎所有瀏覽器都支援這個版本。

## ES6
ES6 又稱 ES2015，做了非常大幅度的更新，新增了 class、async await、arrow function、模組化的功能，這些功能讓這個語言變得更好上手更好使用，現在主流 JavaScript 的樣貌就是 ES6 的樣貌。也是自 2015 年開始 ECMA 決定每一年更新 EcmaScript。

# TypeScript
TypeScript 是由 Microsoft 所開發的語言，簡稱 TS，本質上還是 JavaScript，唯一的不同處如其名，要求變數不得改變其型別。因為 JavaScript 誕生之初的目標受眾是 non-programmer 如網頁設計師，而必須讓這個語言好學好懂好寫，所以設計上不需先行宣告變數型態，然而這是有缺點的。大型程式或多人協作專案可能因為程式碼變數型別管理不易造成 bug。

# Babel
EcmaScript 每年更新但是 Browser 的支援進度跟不上，而 Developers 又是喜新厭舊的人群，該怎麼辦呢？

雖然 interpreter 還未支援新的語法，但其實新的語法可以原語法實現的，例如 ES5 Array.map 就可以用 for loop 實現。所以我們可以用一個 convertor 將新的語法以原語法重構，這就是 Babel 的功能。因為所有 Browser 都對 ES5 全面支援了，所以我們會將語法轉換成 ES5。

# node.js
Ryan Dahl 在 2009 年發表了 node.js，一個基於 Chrome V8 engine 製作的 run time language，它的出現使得前後端都使用 javascript 得以成真。

注意 node.js 跟前端的 JavaScript 本質上是不一樣的語言。在 client-side 運行的  javascript 是遵行 EcmaScript 規範的語言，不同瀏覽器因為直譯器不同的關係，有些許運行上的差異；而 node.js 的直譯器是 Chrome 的 V8 engine。

# Deno.js
Ryan Dahl 在 node.js 十週年之際，列出了 node.js 的十大缺點，接著發表了 Deno.js 聲稱改進了這些缺點。[^2]Deno.js 最大的特色莫過於它同時也是 TypeScript 的 run time environment，廣受歡迎的 TypeScript 只要使用 Deno.js 就不需要先行編譯成 JavaScript 的語法，可以直接被 Deno.js 運行。

Deno.js 目前雖然還沒有辦法取代 node.js，但它是值得投資的超級新星。

[^2]:Deno 的名稱源自於 node 重新排列。

# npm
npm 是 node.js 套件管理器（node.js package manager），原始作者是 Isaac Z. Schlueter.，目前由 npm, inc. 維護。而 npm inc. 是一家營利公司，2020 年被 microsoft 收購，同年 npm 宣布移入 GitHub。[^1]

[^1]:Github 也為 microsoft 的子公司，此舉被解讀為增加 JavaScript 使用人數。

# React.js
 
React.js 是 Facebook 在 2013 年發表的前端框架。跟據 stack overflow 與 GitHub 調查，react.js 是世界上最活躍的前端框架。

## React.js features:
1. Declarative
2. State and props
3. Single Page Application
4. Client Side Rendering
5. one way data flow
6. component lifecycle
7. virtual dom
8. jsx



當我們的專案需要更多套件的時候必須在專案資料夾下執行 `npm install package`，套件會被下載到專案資料夾內，並且記錄在 package.json 裡面。每個專案的 dependencies 都會被下載到自己的 node_modules 資料夾裡面，並不會污染到 global environment。

React 是 declarative 的工具，意思是我們只要告訴它結果，中間的過程它會自己想辦法。如下面這個例子，這是一個紀錄與顯示 button 被點擊的次數的 component，點擊 button 之後他就會更新 state count 並且重新 render component 以顯示新的數字。

```jsx
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

### Single Page Application

Single Page Application（SPA）是一種前端工程手法，相對於 Multi-Page Application（MPA）。MPA 顧名思義就是以許多 HTML 頁面交替顯示不同內容來與使用者互動，MPA 的致命傷是在不同頁面之間切換時都要進行一次 initial load，造成使用者體驗中斷。而 SPA 則是只有一個 HTML 頁面，所以只需要 initial load 一次，所有的內容更新都由 JavaScript 控制，不再需要重新載入整個頁面。SPA 還有一個優點就是最小化 request 次數，因為每次只更新需要更新的部分，而不是整個頁面，所以期望 request 次數會小於 MPA。

SPA 的主要壞處有二。一是 Search Engine Optimization（SEO）較差，因為 SPA 的初載入時需要等待 JavaScript 把畫面渲染好，這段無畫面的時間可能會長過 search engine 快照的時間，造成 SPA 網站被認為是空的，入口網站公司以延長快照時間來對應，developer 也可以透在 HTML 檔中寫好網站重點資訊來避免。二是 SPA 會導致「上一頁」失效，因為實際畫面只有一頁，而這點可以透過 router 工具來解決。


### Virtual DOM

react.js 在更新 dom 的時候不會為了小小的變動而更新整個 dom，這一切都要歸功於它的一項機制，virtual dom。virtual dom 會比較變更前後的 dom 找出需要被變更的地方再行變更，而不是整個 dom 更新，所以比較有效率。

### JSX

jsx 是一個 mind blowing 的工具，我們可以把做好的 component 當作 html tag 一樣寫在 jsx 裡，這樣的寫法實踐了樂高式的設計，所有的 react compoent 都可以被當作樂高玩具一樣隨插隨用。
```jsx
render(){
  return(
    <div>
      <Component1 />
      <Component2 name="foo" startPoints=10 >
	    <p>lorem ipsum</p>
      <Component2>
    </div>
  )
}
```


==========================================================

<!-- 使用下方 code block 的 npm 指令創建一個 react project。指令中的 npx 是 npm 的一項指令，它可以協助下載所有 dependencies；myapp 是專案名稱。成功創造 react 專案之後在 myapp 之內執行 `npm start` 就可以在開發環境運行 react。

```shell
npx create-react-app myapp
``` -->


<!-- # EcmaScript
EcmaScript 是一個語言的 specification，而 javascript 則是依照 EcmaScript 的規範所實作出來的語言，所以 JavaScript 就是 EcmaScript，我們簡稱 ES。ES 每過一段時間就會更新，當我們會稱第五代為 ES5、第六代為 ES6。ES6 之後因為 javascript 的影響力越來越大所以 ECMA(Ecma International) 決定每年都會更新，例如我們會稱 2021 年發出的版本為 ES2021。

年年更新的 EcmaScript 絕對讓 javascript interpreter 的更新速度跟不上，但 developers 就是喜歡新的功能，所以有了 babel 這樣的工具出現，我們可以盡情地撰寫 ES6 以後的版本，然後在透過 babel 編譯成比較舊版的 ES。 -->

<!-- # REACT TUTORIAL

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
``` -->

<!-- jQuery 就是典型的 Imperative 工具，為了達成一個功能，developer 必須用寫下每一個步驟。Imperative 的好處在於我們可以更掌握底層運作，壞處是 code 會變得繁瑣；declarative 的好處就是 code 更好寫，可讀性也會提高，壞處是相對的就是底層運作被掩蓋住了，遇到高效調教時需要打開 black box。

react.js 在更新 dom 的時候不會為了小小的變動而更新整個 dom，這一切都要歸功於它的一項機制，virtual dom。virtual dom 會比較變更前後的 dom 找出需要被變更的地方再行變更，而不是整個 dom 更新，所以比較有效率。

jsx 是一個 mind blowing 的工具，我們可以把做好的 component 當作 html tag 一樣寫在 jsx 裡，這樣的寫法實踐了樂高式的設計，所有的 react compoent 都可以被當作樂高玩具一樣隨插隨用。
``` JSX
render(){
  return(
    <div>
      <Component1 />
      <Component2 name="foo" startPoints=10 >
	    <p>lorem ipsum</p>
      <Component2 />
    </div>
  )
}
``` -->

<!-- one way data flow 是 react 的運作機制，components 的資料只能往 children nodes 傳下去，不能逆流而上。這個機制是為了確保資料更新不混亂。這個機制的缺點是資料交換很麻煩，所以出現了 state 儲存中心的工具 redux。

component lifecycle 是 component 的生命週期，developer 可以依照需求在 component 的某個生命週期執行對應的指令，lifecycle 的主要分類如下：

2. componentDidMount()
3. componentWillMount()

lifecycle 並非 react 創的特色，html5 的 createElement 也有類似的功能，我們在學習 framework 之餘也應該學習 plain html & javascript。
