# Tutorial 2

上一個教學我們已經學會怎麼使用 ES6 的語法和 npm 了，Let's get into code。

我們會進行 [React.js 官方教學](https://reactjs.org/tutorial/tutorial.html)，在這個教學中我們會完成一個 [Tic Tac Toe 遊戲](https://codepen.io/gaearon/pen/gWWZgR?editors=0010)，並且在這個範例中理解 React.js 的 features。

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