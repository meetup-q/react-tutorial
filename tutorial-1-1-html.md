# HTML

HTML 的全名是 Hypertext Markup Language，中文是超文本標記語言。
有幾件事大家必須知道，這世界上有很多標記語言，
如這篇文章使用的 markdomn 就是標記語言。
HTML 是 Sir Tim Berners-Lee 在 1991 年發明的，爵士也因為這個發明得到圖靈獎的肯定。
HTML 並不算是一種程式碼，它只是文本中的標記，告訴瀏覽器這一段落是代表什麼。
爵士當年創造 HTML 的緣由是要利用網際網路的科技快速地傳播學術文章，
所以我們要知道，一個「網站」其實是就是一篇文章，為了使搜尋引擎更理解它，
我們要用對 HTML tags。但內部網站就算全部都用 `<div>` 也無所謂。

2012 年的倫敦奧運開幕式其中一個橋段就是他用 NeXT 電腦創造 world wide web 的樣子。

![2012 Lodon Olympic](https://www.zdnet.com/a/img/resize/50cec62fb6b4678b84065bf10c69c7c58eaed02f/2014/10/05/d4981f41-4cd8-11e4-b6a0-d4ae52e95e57/berners-lee-olympic-2.png?width=770&fit=bounds&format=pjpg&auto=webp)

![2012 London Olympic](https://www.ft.com/__origami/service/image/v2/images/raw/http%3A%2F%2Fcom.ft.imagepublish.upp-prod-eu.s3.amazonaws.com%2Fc84ee18e-3e4a-11e9-b896-fe36ec32aece?fit=scale-down&source=next&width=700)

# Basic Syntex

HTML 分成上下兩個部分，`<head>` 與 `<body>`，要照順序寫。
`<head>` 的主要功用類似於紀錄的是一個網站的 metadata，`<body>` 則是全部內容。

在我們的這個 tutorial 裡不鑽研使用什麼時候該用哪個 tag，
通常情況我們會使用 `<div>` 來包覆 element，若用到其他 tag 時會額外做講解。

```html

<!doctype html>
<!-- html5 -->
<html lang="en">
<head>
  <meta charset="utf-8">
  <!-- encode -->
  <title>HTML5 Starter Template</title>
  <meta name="description" content="Starter Template">
  <meta name="author" content="Sir Tim Berners-Lee">
  <link rel="stylesheet" href="css/styles.css">
</head>
<body>
  <div id="root" class="nice-div">
    Nice Content
  </div>
  <script src="js/scripts.js"></script>
</body>
</html>

```