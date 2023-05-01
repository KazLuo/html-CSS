# HTML CSS進階

[![hackmd-github-sync-badge](https://hackmd.io/9IRxxLwwTYSIC2Nqjl0FhQ/badge)](https://hackmd.io/9IRxxLwwTYSIC2Nqjl0FhQ)


###### tags: `CSS` `HTML`



>*網頁排版都是有關於容器的設定*


## HTML容器特性:
HTML 容器特性是指在 HTML 中用於組織和包裝其他元素的特殊標籤和屬性。這些容器元素有助於將網頁的不同部分區分開來，提供結構化的方式來呈現網頁內容。

想像一個網頁就像一本書，而容器元素就像書中的章節標題、段落、標題和頁腳等。它們有助於組織和排列內容，使網頁更易於閱讀和理解。

舉例來說， `<div>` 是一個常見的容器元素，它可以用來包裝其他 HTML 元素，並將它們組織在一起。你可以將多個元素放在一個 `<div>` 內，然後對該 `<div>` 應用樣式或添加其他屬性。這樣做可以使相關的內容在外觀上具有一致性，並且更容易進行樣式設定或其他操作。

另外還有 `<span>`、`<section>`、`<header>`、`<footer>` 和 `<nav>` 等容器元素，它們具有不同的用途和特性。例如，`<section>` 可以用於區分網頁內容的不同範疇或主題，`<header>` 和 `<footer>` 可以用於標識網頁的標題和頁腳部分，`<nav>` 可以用於定義網頁的導航區域。

這些容器元素讓我們能夠以結構化的方式組織和呈現網頁內容，使得網頁更易於維護、擴展和理解。同時，它們還可以與 CSS 樣式表和 JavaScript 一起使用，以實現更豐富和交互性的網頁效果。

以下為Yahoo網頁，其網頁是由各種不同大小之容器排版而成

![](https://hackmd.io/_uploads/Ske1N-Y7h.png)

### 補充

以下為幾個常見容器標籤及其使用方法:

| 標籤 | 描述 | 範例 |
| --- | --- | --- |
| `<div>` | 最常用的容器元素，用於組織和分組其他 HTML 元素。 | `<div class="container">...</div>` |
| `<span>` | 用於行內元素（如文本）的包裝。 | `<p>這是一個 <span class="highlight">重點文本</span> 的段落。</p>` |
| `<section>` | 將相關的內容分組在一起，例如文章的章節或主題。 | `<section><h2>章節標題</h2><p>這是章節的內容。</p></section>` |
| `<header>` | 定義頁面的標頭。 | `<header><h1>網站標題</h1>...</header>` |
| `<footer>` | 定義頁面的頁腳。 | `<footer>頁腳內容</footer>` |
| `<nav>` | 定義頁面的導航區域。 | `<nav>導航連結</nav>` |

在 HTML 中，可以使用各種標籤和屬性來設定容器。以下是一些常用的 HTML 容器設定方式：

1.  `<div>`：`<div>` 是最常用的容器元素，用於組織和分組其他 HTML 元素。您可以使用 `class` 或 `id` 屬性來為 `<div>` 元素添加額外的樣式或識別。

```HTML
<div class="container">
    <!-- 其他 HTML 內容 -->
</div>
```
2.  `<span>`：`<span>` 也是一個常用的容器元素，但它通常用於行內元素（如文本）的包裝。同樣，您可以使用 `class` 或 `id` 屬性來為 `<span>` 元素添加樣式或識別。
```HTML
<p>
    這是一個包含 <span class="highlight">重點文本</span> 的段落。
</p>

```
3.  `<section>`：`<section>` 用於將相關的內容分組在一起，例如文章的章節或主題。這有助於組織和語義化網頁的結構。
```HTML
<section>
    <h2>章節標題</h2>
    <p>這是章節的內容。</p>
</section>

```
4.  `<header>`、`<footer>` 和 `<nav>`：這些標籤用於定義頁面的標頭、頁腳和導航區域，它們有助於區分網頁的不同部分。
```HTML
<header>
    <h1>網站標題</h1>
    <!-- 其他標頭內容 -->
</header>

<nav>
    <!-- 導航連結 -->
</nav>

<footer>
    <!-- 頁腳內容 -->
</footer>

```

## CSS Reset

當你在建立網頁時，不同的瀏覽器會有各自的預設樣式。這意味著同一段程式碼在不同的瀏覽器上可能會有不同的外觀，這可能會破壞你原本設計的樣式。為了確保你的網頁在各種瀏覽器上看起來一致，你可以使用CSS reset。

CSS reset的目的是消除瀏覽器預設樣式對你的網頁造成的影響。它會將不同瀏覽器的預設樣式歸零，從一個相同的起點開始。這樣一來，你可以更容易地控制你的網頁外觀，因為你不再受到瀏覽器預設樣式的影響。

使用CSS reset可以解決以下問題：

1.  外觀一致性：不同瀏覽器可能對元素的外觀應用不同的預設樣式，例如字體大小、邊距等。CSS reset可以確保所有瀏覽器從同一個起點開始，這樣你可以更容易地設計一致的外觀。
    
2.  解決樣式覆蓋問題：有時你自定義的樣式可能無法正確應用，因為預設樣式的優先級比較高。CSS reset可以清除預設樣式，讓你的自定義樣式正確生效。
    
3.  跨瀏覽器兼容性：不同瀏覽器可能以不同方式呈現相同的HTML元素，導致網頁在不同瀏覽器上外觀不一致。CSS reset可以將這些差異標準化，確保你的網頁在各種瀏覽器上看起來相同。
    

總之，CSS reset是一種技術手段，用於消除瀏覽器預設樣式對網頁外觀的影響，以實現一致的跨瀏覽器外觀。

以Edge為例，其h1標籤內含有一套預設的CSS設定，在不同的瀏覽器其預設值不同，可能造成設計上的不同步

Edge內建預設值:
![](https://hackmd.io/_uploads/Sk1_9ZFQh.png)

所以這部分可以使用CSS Reset的方式將預設值清除
1. 首先連至 https://meyerweb.com/eric/tools/CSS/reset/
並複製其程式碼至CSS檔案，這邊以style.CSS為例

Edge預設效果:
![](https://hackmd.io/_uploads/B1MaTZt7n.png)

使用CSS Reset效果:
![](https://hackmd.io/_uploads/rJdeRWtX3.png)

**CSS Reset之後我還可以再修改樣式嗎?**

可以的!對於CSS選擇器上有覆蓋的性質，也就是相同標籤下，他會以最新(最後)的樣式屬性為基準顯示在畫面中


## display:block(區塊元素)

在HTML中，區塊元素（Block-level elements）是指用於組織和布局網頁內容的元素。這些元素通常在網頁上佔據一整行，並且會在上下文中形成一個獨立的區塊。

以下是區塊元素的一些特性：

1.  1.  佔據整行：區塊元素通常會佔據其父元素的整個寬度，並在下一行開始顯示。舉例來說，`<div>`、`<p>`、`<h1>`到`<h6>`、`<ul>`、`<ol>`、`<li>`等元素都是區塊元素。
    
2.  獨立區塊：區塊元素會在上下文中形成一個獨立的區塊，與其他元素分開。這使得它們可以方便地用於組織和布局網頁的內容，例如創建頁首、頁尾、側邊欄等。
    
3.  高度、寬度設定：區塊元素的高度和寬度可以透過CSS屬性來設定，例如`height`和`width`。預設情況下，區塊元素的寬度會填滿其父元素的可用空間。
    
4.  可以包含其他元素：區塊元素可以包含其他元素，包括其他區塊元素和行內元素。這允許你在區塊元素內部建立更複雜的結構，以呈現不同的內容和佈局。
    
5.  可以設定邊距和間距：區塊元素可以透過CSS屬性來設定邊距（margin）和間距（padding），從而控制元素與周圍元素之間的空白區域。
    
6.  預設為塊級元素：大多數HTML元素預設情況下都是區塊元素，但也有一些元素預設為行內元素（inline elements），例如`<span>`、`<a>`等。不過，可以透過CSS的`display`屬性來改變元素的顯示方式，將行內元素轉換為區塊元素，或將區塊元素轉換為行內元素。


**如何確認是區塊元素?**
1. 可從網頁點擊右鍵檢查啟動開發者工具進行檢視可以發現CSS樣式中有`display:block`屬性，就是有區塊元素

![](https://hackmd.io/_uploads/H1mh6qjX2.png)

2. 也可藉由CSS檢查其標籤是否有標籤元素，首先在CSS中將所需要檢視的標籤進行設定，這邊使用style.CSS做示範(CSS Reset也包含其中，但先省略)

```CSS
h1,p,a,li
{
	/*設定字體及背景顏色*/
	background : #843535;
	color : #fff;

}
```

效果如下:
![](https://hackmd.io/_uploads/HyHmfoim3.png)


從上面結果中可以發現 `h1` `p` `li`標籤都符合區塊元素的兩個特性佔據整行 & 獨立區塊，而a標籤則不是區塊元素，且在開發者工具中沒有`display:block`,目前知道是行內元素(inline)，會在下一階段進行說明

## display: inline 行內元素

在HTML中，行內元素（Inline elements）是指用於在文本內部插入或包裹其他內容的元素。這些元素不會在網頁上佔據一整行，而是與其他元素內聯（inline）地顯示在同一行。

以下是行內元素的一些特性：

1.  佔據所需空間：行內元素只佔據它們所需的空間，而不會佔據整行。這意味著多個行內元素可以在同一行中顯示，除非空間不足，需要換行。
    
2.  不形成獨立區塊：與區塊元素不同，行內元素不會形成獨立的區塊。它們通常嵌套在區塊元素中，或者在文本內部直接使用。
    
3.  可以包含文本和其他行內元素：行內元素可以包含純文本，也可以包含其他行內元素。例如，`<span>`、`<strong>`、`<em>`、`<a>`等元素都是行內元素，它們可以包裹文本或者其他行內元素。
    
4.  高度、寬度無效：行內元素的高度和寬度設定通常無效，除非通過CSS的`display`屬性將其轉換為`block`或`inline-block`元素。預設情況下，行內元素的寬度會隨著其內容而自動調整。
    
5.  邊距和間距設定有限：行內元素的邊距（margin）和間距（padding）設定在水平方向上有效，但在垂直方向上通常無效。也就是說，行內元素的上下邊距和間距設定不會影響行內元素所在行的排列。
    
6.  預設為行內元素：大多數HTML元素預設情況下都是行內元素，例如`<span>`、`<strong>`、`<em>`、`<a>`等。然而，也可以透過CSS的`display`屬性將其轉換為區塊元素或其他顯示方式。
    
7.  可以設定文字相關屬性：由於行內元素通常用於包裹文本，因此可以應用文字相關的CSS屬性，例如字體大小（font-size）、文字顏色（color）、文字粗細（font-weight）等，以改變文本的外觀。
    

行內元素通常用於將文本嵌入到其他文本中或為文本添加特定的樣式和功能。

**行內元素是可以轉換成區塊元素的嗎?**

可以!相反的區塊元素也可以轉換成行內元素，只需要在CSS中添加
`display:inline/block`就可以了!

以下為區塊元素及內行元素差異及轉換的範例:


style.css:
```css
/* http://meyerweb.com/eric/tools/css/reset/ 
   v2.0 | 20110126
   License: none (public domain)
*/

html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed, 
figure, figcaption, footer, header, hgroup, 
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
	margin: 0;
	padding: 0;
	border: 0;
	font-size: 100%;
	font: inherit;
	vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure, 
footer, header, hgroup, menu, nav, section {
	display: block;
}
body {
	line-height: 1;
}
ol, ul {
	list-style: none;
}
blockquote, q {
	quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
	content: '';
	content: none;
}
table {
	border-collapse: collapse;
	border-spacing: 0;
}

.styleblocka/*新增一個設定檔將a設定為區塊*/

{
	background-color: blueviolet;/*設定背景顏色*/
	color: hsl(0, 68%, 32%);/*設定文字顏色*/
	font-size: 30px;/*設定文字大小*/
	display: block;/*設定為區塊*/
	width: 40px;/*設定寬度*/
}

a

{
	background-color: green;/*設定背景顏色*/
	color: azure;/*設定文字顏色*/

}
.inlinep/*新增一個設定檔將p設定為內行元素*/
{
	background-color: yellow;/*設定背景顏色*/
	color: black;/*設定文字顏色*/
	font-size: 20px;/*設定文字大小*/
	display: inline;/*設定為區塊*/
	width: 40px;/*設定寬度*/

}
p
{
	background-color: rgb(202, 52, 180);/*設定背景顏色*/
	color: black;/*設定文字顏色*/
	font-size: 20px;/*設定文字大小*/
	display: block;/*設定為區塊*/


}

span/*建立一個span標籤設置段落內特定文字樣式*/
{
	color: brown;
	font-size: 40px;

}
```



index.html:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Document</title>
</head>
<body>
    <h1>我是h1</h1>
    <!--這邊使用display:inline將區塊元素轉換成行內元素-->
    <h1 class="inlinep">我是inline的h1標籤</h1>
    <h1 class="inlinep">我是inline的h1標籤2</h1>
    
    <!--這邊使用display:block將行內元素轉換為區塊元素-->
    <a href="#" class="styleblocka">這是block的a標籤</a>
    <a href="#">我是原本(inline)的a標籤</a>

    <!--段落中插入span及a標籤-->
    <!--這兩個標籤都有行內元素特性，可以與區塊元素組合運作-->
    <p><span>今天</span>又是個大晴天，不知道什麼時候才會下雨呢?還是來看看<a href="https://tw.news.yahoo.com/weather">天氣預報</a>吧!</p>
   
</body>
</html>
```

效果如下:
![](https://hackmd.io/_uploads/By73Bf6Xh.png)

上面的範例中成功的將區塊元素及行內元素做轉換，以及使用行內元素於區塊元素(p)相互作用

**什麼是`＜span>`標籤?**

`<span>`是一個HTML元素，用於在文本中標記或包裹特定的部分，以便進行樣式化、腳本處理或添加其他屬性和功能。它是一個行內元素，不會在網頁上佔據一整行。

`<span>`元素通常用於以下情況：

1.  文本修飾：你可以使用`<span>`元素將特定的文字或文本片段包裹起來，以便應用CSS樣式或其他修飾效果。例如，你可以為一段文字設置不同的字體顏色、背景色或字體大小，只需要將該段文字包裹在`<span>`標籤中並應用對應的CSS屬性。

```html
<p>這是一個<span style="color: red;">紅色</span>文字。</p>

```

2.  腳本處理：`<span>`元素也可以用於與JavaScript或其他腳本語言進行交互。你可以為特定的文本或文本片段添加`id`或`class`屬性，以便在腳本中操作該元素。例如，你可以通過`id`屬性來選擇並操作特定的`<span>`元素。

```html
<p>請點擊<span id="mySpan" onclick="alert('你點擊了這個<span>元素！');">這個文本</span>。</p>

```

3.  文字分組：有時候，你可能需要將一部分文本視為一個整體進行處理。`<span>`元素可以用作分組容器，使得你可以對這個文本群組應用樣式、添加屬性或進行其他操作。

```html
<p>這個<span class="highlight">文本群組</span>可以應用特殊的樣式。</p>

```

需要注意的是，`<span>`元素本身不會對文本或其內容產生視覺上的影響。它主要用於提供容器或標記，以便在其他元素或腳本中進一步處理。你需要使用CSS或其他手段來為`<span>`元素定義樣式或添加特殊效果。










