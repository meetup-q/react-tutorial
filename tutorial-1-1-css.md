# CSS

CSS 的全名是 Cascading Style Sheets，中文是階層樣式表。
如果說 HTML 是網頁的骨架，那 CSS 就是網頁的皮膚，
是它讓我們的頁面有色彩。


CSS 的 Layout 很簡單，每一個 element 都是二維方格狀的二維盒子，
網頁就是由一個個盒子狀的 element 組成。
盒子有幾個部分：

1. Content：內容區域，Box 中實際有字有圖的地方。
2. Padding：Box 的邊與內容之間的距離，這一段距離是留白的。
3. Border：Box 的邊，一個 Box 的實際大小包含敘述到此的三個部分。
4. Margin：Box 與 Box 之間的距離，並不是 Box 本體的一部分。

![Box Model](https://rollerblade.tw/wp-content/uploads/2021/05/box-model.png)

# 階層

如果我對一個 element 設定有衝突

# Example

```css
.my-box{
  display: block;
  height: 100px;
  width: 100px;
  padding: 10px;
  border: 1px block solid;
  margin: 3px;
  background-color: rgba(123, 220, 112, 0.5);
}

```
