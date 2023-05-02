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
    
3.  高度、寬度設定：區塊元素的高度和寬度可以透過CSS屬性來設定，例如`height`和`width`。預設情況下，區塊元素的寬度及高度會填滿其父元素的可用空間。
    
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

.red/*建立一個red設置段落內特定文字樣式並在span標籤使用*/
{
	color: red;
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
    <!--在span標籤中插入"red"style並在a標籤中插入target="_blank"彈出視窗-->
    <p><span class="red">今天</span>又是個大晴天，不知道什麼時候才會下雨呢?還是來看看<a href="https://tw.news.yahoo.com/weather" target="_blank">天氣預報</a>吧!</p>
   
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

## div & 後代選擇器

在網頁中時常可以看見並排的連結選項
就目前我們已知的辦法可以使用多個a標籤來達成

![](https://hackmd.io/_uploads/H1uGzNC73.png)

但是在大量管理又尤其需要管理樣式的情況就會有不好管理的情況
這時候就需要div & 後代選擇器來幫忙管理了!

### `<div>`

`<div>`是一種容器標籤，沒有語意，是拿來單純排版用的標籤
想像一個`<div>`就像一個大箱子，你可以把不同的東西放進去。這個箱子可以幫助你把網頁分成不同的部分，就像分隔不同的玩具一樣。

`<div>`是一個特殊的HTML元素，它可以讓你將其他元素放在一起，並一起控制它們的樣式和排列方式。這就像把不同的積木堆在一起，並一起玩。

這些是`<div>`元素的一些特性：

1.  包容其他元素：就像箱子可以裝很多東西一樣，`<div>`可以包含其他HTML元素，例如文本、圖片、按鈕等等。你可以把它們放在`<div>`裡面，一起組成一個部分或區域。
    
2.  分隔網頁：就像箱子可以把不同的玩具分開一樣，`<div>`可以幫助你把網頁分成不同的區域或部分。這樣可以更好地組織你的網頁，使它看起來更有秩序。
    
3.  控制樣式：你可以使用CSS（就像你可以為箱子貼上不同的貼紙）來設定`<div>`元素的樣式，例如背景顏色、邊框、間距等等。這樣可以讓你的網頁看起來更漂亮。
    

總結來說，`<div>`就像一個大箱子，可以幫助你將網頁分成不同的部分，並控制它們的樣式和排列方式。它可以包含其他元素，幫助你更好地組織網頁內容，就像分隔不同的玩具一樣。

### 後代選擇器

有時候光是管理`<div>`是不夠的，如果在同一`<div>`標籤中要增加更多樣式的話則會用到後代選擇器!


假設你有一個大家庭，裡面有爸爸、媽媽、兄弟姐妹和你。現在，你想找到只有你和兄弟姐妹的人。你可以使用後代選擇器來完成這個任務。

後代選擇器的使用方式是：你先選擇一個特定的人，然後在這個人的身上找到符合條件的人。就像是你從家族中選擇一個人，然後在他的後代中尋找。

這些是後代選擇器的一些特性：

- 找到特定的元素：後代選擇器可以幫助你找到特定的HTML元素。你可以選擇一個元素，然後在它的後代元素中找到符合條件的元素。

- 嵌套結構：後代選擇器是根據HTML元素的嵌套結構來工作的。就像你家族中的家人是按照父母和子女的關係來組織的一樣，HTML元素也有父元素和子元素的關係。

- 選擇特定層級：後代選擇器可以讓你選擇在特定層級中的元素。比如，你可以選擇某個父元素下的子元素，或者更深層次的元素。

- 選擇多個元素：後代選擇器也可以讓你同時選擇多個符合條件的元素。就像你可以找到所有的兄弟姐妹一樣，後代選擇器可以選擇多個元素。

總結來說，後代選擇器可以幫助你找到特定的HTML元素，就像是找尋家族中的特定成員一樣。它根據元素的嵌套結構工作，讓你可以選擇特定層級或多個元素。就像你可以找到只有你和兄弟姐妹的人一樣，後代選擇器可以讓你在HTML文檔中定位到特定的元素。

假設我們有一個網頁上的HTML結構如下：

```html
<div class="family">
  <h2>家庭成員</h2>
  <ul>
    <li class="parent">爸爸</li>
    <li class="parent">媽媽</li>
    <li class="child">哥哥</li>
    <li class="child">弟弟</li>
    <li class="child">姐姐</li>
    <li class="child">妹妹</li>
  </ul>
</div>

```

現在，我們希望使用後代選擇器選擇只有父母和子女的成員。

CSS中可以使用後代選擇器來達到這個目的。例如：

```css
.family .parent {
  color: blue;
}

.family .child {
  color: red;
}

```

這個例子中，我們使用了`.family .parent`和`.family .child`後代選擇器來選擇相應的元素。

-   `.family .parent`選擇了`.family`下面所有的`class="parent"`的元素（爸爸和媽媽），並將它們的文字顏色設置為藍色。
    
-   `.family .child`選擇了`.family`下面所有的`class="child"`的元素（哥哥、弟弟、姐姐和妹妹），並將它們的文字顏色設置為紅色。
    

這樣，使用後代選擇器我們可以根據元素的嵌套關係選擇特定的元素，並對它們應用不同的樣式。

結果就像是只有父母和子女的成員獲得了不同的文字顏色，讓他們在網頁中有不同的標示。

以下為`<div>` 後代選擇器的範例:

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

img /*圖片的大小*/
{
	width: 50px;
	height: 50px;
}

.style1 a /*連結的顏色，使用後代選擇器格式*/

{
	background: purple;
	color: white;

}

.style1 .header/*產生一個後代選擇器套用在標題上*/

{
	background: purple;
	color: white;
	text-align: center;
	font-size: 30px;
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
    <!--使用div容器匡列標題圖片和連結-->
    <!--使用style1樣式設定標題的字體大小和顏色-->
    <!--h1的部分使用了後代選擇器套用 .style .header的css樣式-->
    <!--其餘a標籤部分使用後代選擇器style1 a的css樣式 -->
    <div class="style1" >
        <h1 class="header">唖唬奇魔</h1>
        <img src="https://s.yimg.com/cv/apiv2/social/images/yahoo_default_logo.png" alt="">
        <a href="https://tw.yahoo.com/">首頁</a>
        <a href="https://tw.mail.yahoo.com/?.intl=tw&.lang=zh-Hant-TW">電子信箱</a>
        <a href="https://tw.news.yahoo.com/">新聞</a>
        <a href="https://tw.stock.yahoo.com/">股市</a>
        <a href="https://tw.money.yahoo.com/">理財</a>

    </div>


</body>
</html>
```

顯示效果如下:

![](https://hackmd.io/_uploads/S1yOaE0Xn.png)


## `<Margin>`

想像一個你在寫字的紙上留下空白的邊界，就像是你畫一個框框，但不在框框裡寫字。這個空白的區域就是margin。

margin是指元素周圍的空白區域，就像是元素的外部邊界。它是在元素和其他元素之間留下的一些空間。

這些是margin的一些特性：

1.  空白區域：margin就像是一個看不見的框框，它沒有實際的內容，只是留下一些空白區域。
    
2.  隔離元素：margin可以將元素與其他元素分隔開來，就像是讓它們保持距離的一道隔離線。
    
3.  控制間距：你可以使用margin來控制元素之間的間距。比如，你可以增加一個元素的上方margin，使它與上面的元素保持一段距離。
    
4.  堆疊規則：當兩個元素的margin相遇時，它們不會疊加在一起，而是遵循堆疊規則。如果兩個元素的margin有重疊，則最終的margin將是兩個margin中較大的值。
    

總結來說，margin就像是元素周圍的空白區域，它可以隔離元素、控制元素之間的間距。你可以把它想像成在寫字的紙上留下的空白邊界，讓不同的元素保持一些距離。

以下為Margin的範例:

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
    <div class="box">
        <h1>降膽固醇藥庇脂清膜衣錠不純物超標 5/20回收5萬顆</h1>
        <p>食藥署今天公布，降膽固醇用藥「庇脂清膜衣錠4毫克」在進行安定性試驗時，發現不純物檢驗結果超標，目前還不確定確切成分，不過已要求廠商於5月20日前回收共1批、5萬顆。</p>
        <img src="https://s.yimg.com/ny/api/res/1.2/T5E3_l9s6J2suAoxXXSZsA--/YXBwaWQ9aGlnaGxhbmRlcjt3PTk2MDtoPTYzODtjZj13ZWJw/https://s.yimg.com/os/creatr-uploaded-images/2023-05/a61ea590-e8be-11ed-9fc7-7e46cd93c29e" alt="藥">
        <p class="annotation">食藥署2日公布，降膽固醇用藥庇「脂清膜衣錠4毫克」在進行安定性試驗時，發現不純物檢驗結果超標，將於5月20日前回收共1批、5萬顆。（圖／食藥署提供）</p>
        <p>根據衛生福利部食品藥物管理署公布藥品回收訊息指出，瑩碩生技醫藥股份有限公司的「庇脂清膜衣錠4毫克 Pitanxo F.C. Tablets 4mg」，批號220881的產品，因接獲藥品不良品通報，啟動回收。這個藥品主要用於原發性高膽固醇血症及混合型血脂異常。</p>
        <p>食藥署藥品組科長洪國登今天接受媒體聯訪指出，廠商在安定性試驗時發現不純物檢驗結果超標，但目前還不確定確切成分，仍在調查中。</p>
        <p>不過，由於不純物或多或少都會存在，這款藥品原本設定的標準是不得超過0.1%。洪國登指出，這次回收共1批、5萬顆，1年健保用量約26萬顆、市占率1%，回收應該不會影響用藥。</p>
        <p>此外，洪國登說，同公司其他藥品過去也曾發生類似情形，不過這款藥品沒有回收紀錄，後續視調查結果才能進一步判斷；已要求廠商於5月20日前完成回收作業，並應繳交回收成果報告書及後續預防矯正措施。</p>
    
    
    </div>
</body>
</html>
```

style.css

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

.box {
	width: 500px;/*設定外框整體寬度*/	
	background: #0b0b09;/*設定背景顏色*/
	text-align: center;/*文字圖形內容置中*/
	border: 5px solid #c94040;/*設定外框粗細顏色*/
	margin: auto;/*整個box置中網頁*/
}

.box img
{
	width: 300px;/*設定圖片寬度*/
}
.box h1
{
	color: white;
	font-size: 30px;
	font-weight: bold;/*粗體*/
	margin: 25px;
}

.box p /*對p標籤內文的文字大小顏色設定*/
{
	text-indent: 2em;/*首行缩排*/
	color: white;/*字體顏色*/
	font-size: 20px;
	margin-bottom: 20px;/*段落間距*/
}

.box .annotation/*對圖片註解的文字大小顏色設定*/
{
	color: rgb(184, 164, 140);
	font-size: 15px;
	
}

```

整體效果:

![](https://hackmd.io/_uploads/rJrhnrAQ3.png)

這邊需要補充一下，在網頁設計時可以注意到`<div>`內部只有設計寬度
而不設定高度，這是因為我們要套用區塊元素的特性 **"高度、寬度設定：區塊元素的高度和寬度可以透過CSS屬性來設定，例如`height`和`width`。預設情況下，區塊元素的寬度及高度會填滿其父元素的可用空間。"** 如果我設定好高度可能會出現文字超出高度的問題造成整體網頁不美觀

![](https://hackmd.io/_uploads/HJgJCBCm2.png)


## Padding 留白

剛剛的margin可以針對單一或是多個標籤進行空間推擠產生留白效果
但如果標籤種類眾多的情況下，每種標籤都使用margin會非常麻煩，因此我們可以使用`padding`來做留白的效果

首先我們使用上面的報導做示範:

![](https://hackmd.io/_uploads/r1NueLC7h.png)

從上面可以看到如果我要將左側做留白，那我可以能會要將`<h1>` `<p>` `<img>`內部都加上`margin-left`才可以達到左邊留白的效果:

```css
.box {
	width: 500px;/*設定外框整體寬度*/	
	background: #0b0b09;/*設定背景顏色*/
	text-align: center;/*文字圖形內容置中*/
	border: 5px solid #c94040;/*設定外框粗細顏色*/
	margin: auto;/*整個box置中網頁*/
}

.box img
{
	width: 300px;/*設定圖片寬度*/
	margin-left: 20px;/*設定圖片與文字間距*/
}
.box h1
{
	color: white;
	font-size: 30px;
	font-weight: bold;/*粗體*/
	margin: 25px;
	margin-left: 20px;/*設定圖片與文字間距*/
}

.box p /*對p標籤內文的文字大小顏色設定*/
{
	text-indent: 2em;/*首行缩排*/
	color: white;/*字體顏色*/
	font-size: 20px;
	margin-bottom: 20px;/*段落間距*/
	margin-left: 20px;/*設定圖片與文字間距*/
}

.box .annotation/*對圖片註解的文字大小顏色設定*/
{
	color: rgb(184, 164, 140);
	font-size: 15px;
	margin-left: 20px;/*設定圖片與文字間距*/
	
}
```

但如果我們使用`padding`只需要在"box"內部加上就可以呈現內容左側留白效果:

```css
.box {
	width: 500px;/*設定外框整體寬度*/	
	background: #0b0b09;/*設定背景顏色*/
	text-align: center;/*文字圖形內容置中*/
	border: 5px solid #c94040;/*設定外框粗細顏色*/
	margin: auto;/*整個box置中網頁*/
	padding-left: 20px;/*設定左側內距*/
}
```

![](https://hackmd.io/_uploads/By7MfI0Qh.png)


**四邊留白效果**

```css
.box {
	width: 500px;/*設定外框整體寬度*/	
	background: #0b0b09;/*設定背景顏色*/
	text-align: center;/*文字圖形內容置中*/
	border: 5px solid #c94040;/*設定外框粗細顏色*/
	margin: auto;/*整個box置中網頁*/
	padding: 20px;/*四側留白效果*/
}
```
![](https://hackmd.io/_uploads/HkU5GIAX2.png)




## Box Model

盒模型（Box Model）是一種描述HTML元素佔用空間和佈局的概念。它將每個元素視為一個矩形的盒子，並定義了該盒子的各個部分。

盒模型包含以下四個主要部分：

1.  內容區域（Content Area）：盒子的內容部分，通常是文字、圖片或其他內容。
    
2.  內邊距（Padding）：內邊距是內容區域與邊框之間的空白區域。它可以用來控制元素內容與邊框之間的間距。
    
3.  邊框（Border）：邊框是包圍內容和內邊距的線條或區域。它可以設置邊框的顏色、寬度和樣式。
    
4.  外邊距（Margin）：外邊距是邊框與其他元素之間的空白區域。它可以用來控制元素與其他元素之間的間距。
    

下圖是一個示意圖，展示了盒模型的各個部分：

![](https://hackmd.io/_uploads/rJTMhLAmn.png)

以下為示意圖所顯示的效果及程式碼:


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

.box {
	width: 300px;
	height: 300px;
	margin: 10px;
	padding: 50px;
	border: 5px solid #9231ab;
	background: #3c44a1;
}
.box2 {
	width: 300px;
	height: 300px;
	margin: 20px;
	padding: 70px;
	border: 10px solid #9231ab;
	background: #3c44a1;
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
    <p class="box">
    width: 300px;
	height: 300px;
	margin: 10px;
	padding: 50px;
	border: 5px solid #9231ab;
	background: #3c44a1;
    </p>
    <p class="box2">
        width: 300px;
	height: 300px;
	margin: 20px;
	padding: 70px;
	border: 10px solid #9231ab;
	background: #3c44a1;
    </p>
</body>
</html>
```
效果如下:

![](https://hackmd.io/_uploads/B1W8kvRXh.png)

比較一下兩者的差異，可以發現，實際影響方格尺寸除了本體的長寬之外還有`padding`及`border`的大小。雖然`Margin`不同，但是他僅影響網頁上方塊的位置，並不影響實際方格尺寸

盒模型是網頁設計中重要的概念，它幫助我們理解和控制元素在佈局中的位置和外觀。通過調整盒模型的相關屬性，我們可以實現各種各樣的佈局和設計效果。
























