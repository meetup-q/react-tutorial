# Tutorial 2: tic-tac-toe game

上一個教學我們已經學會怎麼使用 ES6 的語法和 npm 了，Let's get into code。

我們會進行 [React.js 官方教學](https://reactjs.org/tutorial/tutorial.html)，在這個教學中我們會完成一個 [Tic Tac Toe 遊戲](https://codepen.io/gaearon/pen/gWWZgR?editors=0010)，並且在這個範例中理解 React.js 的 features。

- [Tutorial 2: tic-tac-toe game](#tutorial-2-tic-tac-toe-game)
- [Tic Tac Toe Game](#tic-tac-toe-game)
  - [create react app](#create-react-app)

# Tic Tac Toe Game

## create react app
首先我們使用 npm 的附屬指令 npx 發動 create-react-app，npx 會搜尋全域變數中有無 create-react-app，若無則會先下載這個套件，使用完之後刪除。npx 是一個相當就手的指令，因為多數時候我們只需要某一個工具一次，做用完成之後即不需要。

```shell
npx create-react-app myapp
```
下載完成之後，我們可以會在 command line 的最下方看到 `happy coding`，這就表示初始成功，趕緊用下方的指令試行。

```shell
npm start
```

使用下方 code block 的 npm 指令創建一個 react project。指令中的 npx 是 npm 的一項指令，它可以協助下載所有 dependencies；myapp 是專案名稱。成功創造 react 專案之後在 myapp 之內執行 `npm start` 就可以在開發環境運行 react。
```shell
npx create-react-app myapp
```

當我們的專案需要更多套件的時候必須在專案資料夾下執行 `npm install package`，套件會被下載到專案資料夾內，並且記錄在 package.json 裡面。每個專案的 dependencies 都會被下載到自己的 node_modules 資料夾裡面，並不會污染到 global environment。



``` javascript
class Square extends React.Component {
  render() {
    return (
      <button className="square">
        {/* TODO */}
      </button>
    );
  }
}

class Board extends React.Component {
  renderSquare(i) {
    return <Square />;
  }

  render() {
    const status = 'Next player: X';

    return (
      <div>
        <div className="status">
          {status}
        </div>
        <div className="board-row">
          {this.renderSquare(0)}
          {this.renderSquare(1)}
          {this.renderSquare(2)}
        </div>
        <div className="board-row">
          {this.renderSquare(3)}
          {this.renderSquare(4)}
          {this.renderSquare(5)}
        </div>
        <div className="board-row">
          {this.renderSquare(6)}
          {this.renderSquare(7)}
          {this.renderSquare(8)}
        </div>
      </div>
    );
  }
}

class Game extends React.Component {
  render() {
    return (
      <div className="game">
        <div className="game-board">
          <Board />
        </div>
        <div className="game-info">
          <div>{/* status */}</div>
          <ol>{/* TODO */}</ol>
        </div>
      </div>
    );
  }
}

ReactDOM.render(
  <Game />,
  document.getElementById('root')
);

```


one way data flow 是 react 的運作機制，components 的資料只能往 children nodes 傳下去，不能逆流而上。這個機制是為了確保資料更新不混亂。這個機制的缺點是資料交換很麻煩，所以出現了 state 儲存中心的工具 redux。

component lifecycle 是 component 的生命週期，developer 可以依照需求在 component 的某個生命週期執行對應的指令，lifecycle 的主要分類如下：
1. 
2. componentDidMount()
3. componentWillMount()

lifecycle 並非 react 創的特色，html5 的 createElement 也有類似的功能，我們在學習 framework 之餘也應該學習 plain html & javascript。