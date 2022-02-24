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

樣式有以下幾種階級
1. inline style → 最優先，應該要最少用，避免維護困難
2. id → 次優先，常用
3. class → 最常用，善用 class 可以減少 CSS 維護難度
4. element → 優先度最低，利用來設定基底的樣式

假如我重複設定一個 id 的樣式會發生什麼事情呢？
CSS 是逐行直譯的，當它再讀到同樣的 CSS 會複寫舊的。

```css
#my-id{
  height: 100px;
}

/* ~~~ */

#my-id{
  height: 80px;
}
/* #my-id 的高度 height 就是 80px */
```


# Example

```css
#my-id{
  height: 100px;
}

.my-box{
  display: block;
  height: 100px;
  width: 100px;
  padding: 10px;
  border: 1px block solid;
  margin: 3px;
  background-color: rgba(123, 220, 112, 0.5);
}

nav{
  width: 100%;
  height: 50px;
}
```

```html
<div id="my-id" style="height: 10px"></div>
<!-- 因為 inline style 存在，他的優先度最高，所以 height 是 10px -->
```
