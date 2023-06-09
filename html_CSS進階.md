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


### 補充

當您將一個子元素設定為 `display: block;` 時，它會變成一個塊級元素，並且預設會佔據其父元素的寬度。這表示如果您的父元素也是一個塊級元素（例如 `div`），且沒有設定寬度，那麼子元素的寬度就會與父元素相同。

以下是一個範例，可以幫助您理解這個行為：

```htmle
<div>
  <p>這是一個段落。</p>
</div>

```

```css
div {
  border: 1px solid black;
}

p {
  display: block;
  border: 1px solid red;
}

```

在上述範例中，我們將 `p` 元素設定為 `display: block;`，並且在 `div` 元素中包含它。由於 `div` 元素本身也是一個塊級元素，因此 `p` 元素的寬度就會與 `div` 元素相同。

如果您希望子元素的寬度不受父元素的影響，可以使用其他的 `display` 值（例如 `inline-block` 或 `inline`），或是給父元素和子元素都設定一個寬度。




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


## 子元素選擇器

**css 中 .row >div {} 中的">"是什麼意思**

在 CSS 中，`>` 符號是稱為「子元素選擇器」（Child Selector）的一種選擇器，它可以選取指定元素的直接子元素。

例如，`.row > div` 就是選擇所有 `.row` 元素的直接子元素中是 `div` 的元素。這表示，只有在 `.row` 直接包含 `div` 元素時，這個選擇器才會生效。如果 `.row` 元素包含了其他元素（例如另一個 `.row` 元素），這些元素就不會被選取到。

以下是一個簡單的範例，展示了子元素選擇器的用法：

```html
<div class="row">
  <div>這是第一個 div 元素。</div>
  <p>這是一個段落。</p>
  <div>這是第二個 div 元素。</div>
</div>
```

```css
.row > div {
  background-color: yellow;
}
```
![](https://hackmd.io/_uploads/ryhuTCtE3.png)



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


### 補充

**`margin:auto`和`margin-left:auto` & `margin-right:auto`的差異性**

如果只是將元素水平置中，並且沒有其他特殊需求，我建議使用 `margin: auto;`，因為它簡潔、易讀且達到相同的效果。如果你需要更多的控制或特定對齊需求，那麼使用 `margin-left: auto;` 和 `margin-right: auto;` 可能更適合。選擇哪一種方法取決於你的具體需求和個人喜好。

**text-align:center 文字置中**

可藉由text-align使文字達到置中效果，先看以下範例:

![](https://hackmd.io/_uploads/SkjYZj1N3.png)


以上範例我使用`<div>`標籤做出父階級名為"wrap"，並做出子階級
"header"、"content"、"footer"分別做出頁首內文及頁腳，這邊需要注意的是由於我在"wrap"中已經設定其寬度，依照區塊元素特性，其餘子階級皆會使其空格填滿，因此子階級的部分皆不須調整寬度。
以下會補充一下之前未提到的標籤及CSS語法

- `<br>`:用於斷行作用，可穿插在`<p>`標籤內座使用

```html
      <div class="footer">
            <p>聯絡地址:高雄市苓雅區永定街99號44F
                <!--這邊使用br標籤做斷行-->
                <br>連絡信箱:ccc1234@gmail.com
            </p>       
            <p>連絡電話:09112345678</p>
        </div>
```

- `text.align`:這部分我用在頁首/內文/頁尾皆有用到，主要用於將文字置中達成排版較為舒適的觀看體驗

- `line-height`:這邊用於內文設定`<p>`標籤內文的行寬，在設定上可以使用pixel或是幾倍行寬(1.5)來設定






以下為範例程式碼:

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
    <div class="wrap">
        <div class="header">
            <h1>我是標題</h1>
        </div>
        <div class="content">
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Error praesentium debitis nobis, placeat nisi similique pariatur esse enim hic autem delectus. Sed, expedita numquam est iste molestiae asperiores officiis voluptatum!</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Error praesentium debitis nobis, placeat nisi similique pariatur esse enim hic autem delectus. Sed, expedita numquam est iste molestiae asperiores officiis voluptatum!</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Error praesentium debitis nobis, placeat nisi similique pariatur esse enim hic autem delectus. Sed, expedita numquam est iste molestiae asperiores officiis voluptatum!</p>
        </div>
        <div class="footer">
            <p>聯絡地址:高雄市苓雅區永定街99號44F
                <!--這邊使用br標籤做斷行-->
                <br>連絡信箱:ccc1234@gmail.com
            </p>       
            <p>連絡電話:09112345678</p>
            
        </div>
    </div>


</div>
   
</body>
</html>

```

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

.wrap
{
	width: 600px;/*由於父階層已經設定600px,所以以下子階層就不須設定*/
	margin: auto;/*讓整個網頁置中*/
}
.header
{
	background-color: rgb(217, 201, 137);
	height: 50px;
}
.header h1
{
	text-align: center;/*文字置中*/
	line-height: 50px;
	font-size: 50px;
}
.content
{
	background-color: rgb(185, 205, 138);
	padding-top: 10px;/*上方留白*/
	padding-bottom: 10px;/*下方留白*/
}
.content p
{
	font-family: 'Times New Roman', Times, serif;/*字型*/
	text-align: center;/*文字置中*/
	line-height: 1;/*行高*/
	font-size: 30px;
	margin-bottom: 15px;
	padding-top: 10px;
	padding-bottom: 10px;
}
.footer
{
	background-color: rgb(207, 189, 115);
	text-align: center;
	padding-top: 10px;
	padding-bottom: 10px;
}
```

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

## Box-sizing:border-box

如果在Box-Model使用上覺得不直覺，可以在css中加入`box-sizing:border-box`
它會依照你初始設定的長寬將其pedding及border向內縮，也就不需要再去計算加入padding及border後的長寬值了!

先看效果:

![](https://hackmd.io/_uploads/Sk4MCiyVh.png)


這邊可以注意到在一樣添加`border:10px`及`padding:10px`在沒有
`box-sizing:border-box`的大小就會未添加後的還要多出40，且添加後的長寬值與初始設定值大小不變

以下為程式碼:

index.html:

```htmle
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
<div class="box">Total:200*200</div>
<div class="box1">200*200<br>padding:10*2<br>border:10*2<br>Total:240*240</div>
<div class="box2">200*200<br>padding:10*2<br>border:10*2<br>Total:200*200<br>box-sizing: border-box</div>
</body>
</html>
```

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

.box
{
	width: 200px;
	height: 200px;
	background-color: red;
	margin: 10px;
	text-align: center;
}

.box1
{
	width: 200px;
	height: 200px;
	background-color: red;
	padding: 10px;
	border: 10px solid black;
	margin: 10px;
	text-align: center;
}

.box2
{
	width: 200px;
	height: 200px;
	background-color: blue;
	padding: 10px;
	border: 10px solid black;
	margin: 10px;
	box-sizing: border-box;
	text-align: center;
}

```

### 補充

**假如我今天想讓所有HTML標籤都吃相同的屬性怎麼辦?**


從剛剛的方格我們可以注意到box1及box2大小是不一樣的，假若我今天想要全部統一我們可以加入這段程式碼在前面:


```css
*, *:before, *:after {
  box-sizing: border-box;
}
```

效果如下:

![](https://hackmd.io/_uploads/H1_8yh1Eh.png)

也就是說我們讓所有的HTML標籤都吃到了`box-sizing: border-box`的效果。

說明一下這段程式的意思:

**`*, *:before, *:after{}`**

這段程式碼 `*, *:before, *:after {}` 是一個 CSS 選擇器，它選擇了所有元素以及它們的 `::before` 和 `::after` 偽元素。使用這個選擇器，可以方便地對所有元素及其偽元素應用一組共同的樣式。這在設定全域樣式、重置樣式或者統一調整元素的外觀時很有用。

**什麼是偽元素?**

當你在畫一幅圖畫時，你可以用不同的顏色和材料來裝飾整個圖畫。有時候，你可能想要在圖畫上添加一些特殊的東西，但你又不想去修改已經畫好的部分。這時，你可以使用一些額外的紙張或特殊的顏料，並把它們放在圖畫的某個特定位置上，以增加一些額外的細節。在網頁設計中，偽元素就像是這些額外的紙張或特殊的顏料。它們是一些特殊的指令，讓我們可以在元素的某個特定位置上添加一些額外的元素或樣式，而不需要修改原始的 HTML 標記。舉個例子，假設你有一個段落（`<p>`）元素，你想要在該段落的開頭添加一個特殊的符號或圖標。這時，你可以使用偽元素 `::before`，它允許你在段落的開頭添加一個額外的元素，並對它應用特殊的樣式。

偽元素使用雙冒號 `::` 作為標示符號，用於區分於偽類（pseudo-class）。在舊版的 CSS 中，單冒號 `:` 也被用於表示偽元素，但在 CSS3 中推薦使用雙冒號 `::`。

偽元素可以在元素的內容之前或之後生成額外的元素，並對其應用樣式。它們不是真正的 HTML 元素，而是通過 CSS 選擇器和樣式來模擬生成的。

常見的偽元素包括：

1.  `::before`：在元素內容的前面生成一個額外的元素。
2.  `::after`：在元素內容的後面生成一個額外的元素。
3.  `::first-line`：選擇元素的第一行文字。
4.  `::first-letter`：選擇元素的第一個字母。

**`*, *:before, *:after {}`中的"*"是什麼意思?**

在 CSS 中，`*` 符號表示通用選擇器（universal selector），也被稱為全局選擇器。它選擇了所有的元素，無論是 `<div>`、`<p>`、`<img>` 或其他任何元素都包括在內。

當 `*` 用於 `*, *:before, *:after {}` 的選擇器中時，它表示選擇所有的元素，包括偽元素 `::before` 和 `::after`。這樣的選擇器是一種通用的選擇器，用於對所有元素及其偽元素應用相同的樣式。

使用 `*` 選擇器可以方便地一次性選擇所有的元素，並對它們應用相同的樣式。在這個例子中，`*, *:before, *:after {}` 是一個 CSS 規則集，它指定了這些選擇器所選擇的元素和偽元素的樣式設定。這種方式可以用來重置或統一所有元素的樣式，或者給它們添加一些共同的屬性，以節省編寫單獨選擇器的時間和代碼量。


# Flex 網頁排版技巧
以下為Flex結構
```
-----------------------------------------------------
|                 Flex Container                    |
|---------------------------------------------------|
|        Flex Item        |       Flex Item         |
|---------------------------------------------------|
|        Flex Item        |       Flex Item         |
|---------------------------------------------------|
```
在這個結構中，Flex Container（彈性容器）是最外層的容器，它包含了一個或多個Flex Item（彈性項目）。彈性容器的主要作用是決定Flex Item在主軸和交叉軸上的排列方式和對齊方式。

Flex Item則是放置在彈性容器內的元素，可以是文字、圖片、區塊等。這些彈性項目可以根據彈性容器的設定在主軸和交叉軸上進行排列和對齊。

總結來說，Flex布局提供了一個彈性的容器和項目結構，使我們能夠靈活地控制元素的佈局和對齊方式。透過調整彈性容器的屬性，我們可以創建各種不同的佈局效果。

Flex布局具有以下特性：

1.  彈性尺寸調整：Flex容器內的彈性項目可以按照比例自動調整尺寸，以填滿或縮小容器的可用空間。
    
2.  主軸和交叉軸控制：Flex容器可以設定主軸方向（水平或垂直），並控制彈性項目在主軸和交叉軸上的排列和對齊方式。
    
3.  彈性順序調整：Flex項目可以通過調整彈性順序（order）屬性來改變它們在容器中的排列順序。
    
4.  自動換行：當Flex項目在一行或一列上無法容納時，它們可以自動換行到下一行或下一列，以適應容器的大小。
    
5.  對齊和間距控制：Flex容器可以控制彈性項目在主軸和交叉軸上的對齊方式，並設定彈性項目之間的間距。
    
6.  嵌套支持：Flex容器可以嵌套在其他Flex容器內，形成更複雜的佈局結構。



## Flex 外層屬性 (container) 



當我們談到 Flex 外層屬性時，我們是指在使用 Flex 布局時，將這些屬性應用於包含 Flex 元素的容器（也就是外層元素）上的一組屬性。

Flex 外層屬性是一組可以控制元素在 Flex 容器中排列方式和對齊方式的屬性。這些屬性可以幫助我們建立靈活的布局，使元素能夠按照我們的需求在頁面上排列。

Flex 外層屬性包括：

1.  `display: flex;`：這個屬性告訴瀏覽器將容器設置為 Flex 容器，以便我們可以使用 Flex 布局。
    
2.  `flex-direction`：這個屬性用於指定元素在 Flex 容器中的排列方向，可以是水平方向（從左到右或從右到左）或垂直方向（從上到下或從下到上）。
    
3.  `justify-content`：這個屬性用於控制元素在 Flex 容器的主軸上的對齊方式，包括靠左、靠右、居中等。
    
4.  `align-items`：這個屬性用於控制元素在 Flex 容器的交叉軸上的對齊方式，包括靠上、靠下、居中等。
    
5.  `flex-wrap`：這個屬性用於指定元素是否可以換行，當元素的總寬度或高度超過 Flex 容器時，是否將元素換到下一行或下一列。
    

總而言之，Flex 外層屬性是一組用於控制 Flex 容器中元素排列方式和對齊方式的屬性。這些屬性可以幫助我們創建靈活的布局，讓元素能夠按照我們的需求在頁面上排列。

以下我會設置一個未使用flex排版的效果，並比較使用flex排版後的效果

使用前:

![](https://hackmd.io/_uploads/SkYiFlZ4n.png)


以下是我設計的參數

容器(container):
```css
	width: 500px; /*設定寬度500px，這邊不設定高度*/
	background: #416222;
	margin: 0 auto;
	padding : 10px;
	
```


物品(item):
```css
.item /*設定項目*/
{
	width: 100px; /*設定item寬度*/
	background: #000;/*設定item背景顏色*/
	color:aliceblue;/*設定item文字顏色*/
	font-size: 20px;
	margin: 10px;
	text-align: center;
	
}
.item1 /*設定後代選擇器 item1*/
{
	height: 400px;/*這邊設定item1的高度*/
	background: #a01a1a;

}
.item2/*設定後代選擇器 item2*/
{
	width: 200px;/*這邊設定item2的高度*/
	height: 300px;
}
.item3/*設定後代選擇器 item3*/
{
	width: 600px;/*這邊故意將item3的寬度設定超出容器的寬度*/
	background:#3564cb
}
```

這邊有幾個要注意的地方:
- 容器寬度為500px
- item1&2的高度分別為400px&200(item3照文字大小自適應)
- item3寬度為600px(超出容器)
- 因區塊元素特性其區塊無並排，接獨佔一列


接著我在容器container(父階級)添加`display:flex` 產生Flex排版
效果如下:

![](https://hackmd.io/_uploads/HynN5gWE2.png)

可以明顯感受到添加flex排版後的差異

- item都變成並排
- item3的高度上因為沒有設定而自適應成最大設定高度(item1:400px)
- item3的寬度原先超出容器(容器:500px item3:600px)使用Flex後自動彈性縮排將3者分配在容器中
- item2因為有設定高度，因此沒有自適應成一樣的高度

因此我們可以總結一下`display:flex`的特性:

- 可以將區塊元素佔據一行的特性取消，並使其能夠產生並排
- 可以將超出容器的item彈性限縮於容器並依比例進行分配
- 沒有特別設定寬高的item會自適應item中最大值進行同步

最後附上程式碼:

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


.container /*設定容器*/

{
	width: 500px; /*設定寬度，這邊不設定高度*/
	background: #416222;
	margin: 0 auto;
	padding : 10px;
	display: flex;	
	
}

.item /*設定項目*/
{
	width: 100px; /*設定item寬度*/
	background: #000;/*設定item背景顏色*/
	color:aliceblue;/*設定item文字顏色*/
	font-size: 20px;
	margin: 10px;
	text-align: center;
	
}
.item1 /*設定後代選擇器 item1*/
{
	height: 400px;/*設定item1的高度*/
	background: #a01a1a;

}
.item2/*設定後代選擇器 item2*/
{
	width: 200px;
	height: 300px;/*設定item2的高度*/
}
.item3/*設定後代選擇器 item3*/
{
	width: 600px;/*這邊故意將item3的寬度設定超出容器的寬度*/
	background:#3564cb
}
```

index.html

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
    <div class="container">
        <div class="item item1">1</div>
        <div class="item item2">2</div>
        <div class="item item3">3</div>
    </div>

</body>
</html>
```

### 補充
From:六角學院
關於Flex排版的模擬器
[Flexbox Playground (codepen.io)](https://codepen.io/peiqun/pen/WYzzYX)


## flex-direction - 決定 flex 軸線

`flex-direction` 是一個用於控制 Flex 容器中彈性項目排列方向的屬性。它可以設定彈性項目在主軸（水平軸）或交叉軸（垂直軸）上的排列方式。以下是 `flex-direction` 的幾種設定及其特性：

1.  `row`: 彈性項目水平排列，從左到右。
```
┌───┬───┬───┐
│ 1 │ 2 │ 3 │
└───┴───┴───┘
``` 
2.  `row-reverse`: 彈性項目水平排列，從右到左。
    
```
┌───┬───┬───┐
│ 3 │ 2 │ 1 │
└───┴───┴───┘
```
3.  `column`: 彈性項目垂直排列，從上到下。
```
┌───┐
│ 1 │
├───┤
│ 2 │
├───┤
│ 3 │
└───┘
```
4.  `column-reverse`: 彈性項目垂直排列，從下到上。
```
┌───┐
│ 3 │
├───┤
│ 2 │
├───┤
│ 1 │
└───┘

```
透過設定不同的 `flex-direction` 值，我們可以控制彈性項目的排列方向，達到不同的版面配置效果。注意在使用flex排版的前提都必須在容器(父階層)新增`display:flex`才可以正常運作

```css
.container 
{
	width: 500px;
	background: #0d3f55;
	margin: 0 auto;
	padding:10px;
	display:flex;
	flex-direction: row;
}
```

### 補充

這邊要特別說一下使用`flex-direction`本身不只影響容器內的item排序也會影響其排版，以`flex-direction:row / row-reverse`為例:

flex-direction:row

![](https://hackmd.io/_uploads/SkYV_Hz42.png)

flex-direction:row-reverse

![](https://hackmd.io/_uploads/ByvyOBGEn.png)

## justify-content: 決定主軸對齊方式
justify-content是flexbox布局中的一個屬性，用於調整彈性容器（flex container）中的子元素（flex items）在主軸（水平軸）方向上的對齊方式。

以下是justify-content的幾種常見取值及其特性：

1.  flex-start：將子元素在主軸的起始位置對齊。

2.  flex-end：將子元素在主軸的結束位置對齊。
    
3.  center：將子元素在主軸的中心位置對齊。
    
4.  space-between：將子元素平均分布在主軸上，首尾子元素貼緊彈性容器的起始和結束位置。
    
5.  space-around：將子元素平均分布在主軸上，使得每個子元素周圍有相等的空間。
    
6.  space-evenly：將子元素平均分布在主軸上，使得每個子元素之間和周圍的空間都相等。


這些取值可根據需求選擇，用於調整彈性容器中的子元素在主軸上的對齊方式，從而達到不同的布局效果。

![[CSS justify-content - Scaler Topics](https://www.scaler.com/topics/css-justify-content/)
](https://hackmd.io/_uploads/rJD4CHMVn.png)
*form:[CSS justify-content - Scaler Topics](https://www.scaler.com/topics/css-justify-content/)*

目前Flex所學習到都是針對容器去做修改，僅附上容器程式碼:

```css
.container 
{
	width: 500px;
	background: #0d3f55;
	margin: 0 auto;
	padding:10px;
    /*使用Flex排版*/
	display:flex;
    /*選擇其主軸排序的方式*/
	flex-direction: row;
    /*選擇其對其的方式`,這邊使用space-between*/
	justify-content: space-between;
	

}
```
效果如下:

![](https://hackmd.io/_uploads/BJSFrLMN2.png)


比較未加`justify-content` :

![](https://hackmd.io/_uploads/ByHiHLfN2.png)


**如果今天我想做垂直對齊該怎麼做?**

可以將主軸由row改為column即可，這邊一樣使用space-between效果:


```css
.container 
{
	width: 500px;
	background: #0d3f55;
	margin: 0 auto;
	padding:10px;
    /*使用Flex排版*/
	display:flex;
    /*選擇其主軸排序的方式*/
	flex-direction: column;
    /*選擇其對其的方式`,這邊使用space-between*/
	justify-content: space-between;
	

}
```

![](https://hackmd.io/_uploads/SyGlEgUNh.png)

## 使用FLEX進行排版

做出下面的排版方式
![](https://hackmd.io/_uploads/BkXMKWU4h.png)

網頁需求
 - 各連結以並排的方式呈現(display:flex)
 - 網頁的選單方格判定寬裕(padding)
 - 滑鼠移動過去時有變色效果(hover)
 - 文字置中(text-align)

1. 各連結以並排的方式呈現(display:flex)
在外層容器中添加`display:flex`使他產生flex排版
因原始flex排版已經制定排版方式為row，不須添加`flex-direction:row`



2. 網頁的選單方格判定寬裕(padding)
如果連結中部使用`display:block`時，因連結非區塊元素造成連結沒有填滿效果
```css
.container li a
{
	/*display: block;*/
	padding-top: 10px;
	padding-bottom: 10px;
	background: #34697a;
	text-decoration: none;
	color: white;
}
```
未使用display:block
![](https://hackmd.io/_uploads/SyrV-fIE2.png)
使用display:block
![](https://hackmd.io/_uploads/BJ_mMf8Vn.png)

3. 滑鼠移動過去時有變色效果(hover)

在a標籤中加上顏色，在滑鼠移動至連結時改變顏色(hover)

```css
.container li a:hover
{
	background: #cea04b;
}
```


![](https://hackmd.io/_uploads/S1kPQz8N2.png)

附上完整程式碼:

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
 <ul class="container">
    <li class="item"><a href="#">首頁</a></li>
    <li class="item"><a href="#">政治</a></li>
    <li class="item"><a href="#">政壇</a></li>
    <li class="item"><a href="#">財經</a></li>
    <li class="item"><a href="#">娛樂</a></li>
 </ul>
</body>
</html>
```

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

.container

{
	width: 600px;
	margin:0 auto;
	display: flex;
	}

.container li
{
	width: 100px;
	border: 1px solid black;
	text-align: center;
}

.container li a
{
	display: block;
	padding-top: 10px;
	padding-bottom: 10px;
	background: #34697a;
	text-decoration: none;
	color: white;
}
.container li a:hover
{
	background: #cea04b;
}
```

## flex-warp

flex-warp可以做到網頁換行效果:

![](https://hackmd.io/_uploads/SkfX3fUN2.png)


使用方式在容器的部分中添加flex-warp:warp進行換行

```css
.container

{
	width: 600px;
	margin:0 auto;
	display: flex;
	flex-wrap: wrap;
}
```
原理為當元件寬度超過600px時會自動將其餘元件進行換行

**width 600 px的情況為何第六個就進行換行?**

雖然每一個`li`的寬度為100但，因為`border(10 px)`本身也算在整個容器寬度內，第五個元件時已經達到寬度上限，因此第六個元件會進行換行動作

## 交錯軸排序(align-items)

如果說justify-content是針對主軸的排序，align-items就是針對垂軸的排序進行調整，其種類有以下五種

`align-items` 是一個 CSS 屬性，用於定義 Flex 容器內的 Flex 子元素在交錯軸（Cross Axis）上的對齊方式。它有以下幾種屬性值：

1.  `stretch`：預設值，讓 Flex 子元素在交錯軸上拉伸填滿整個 Flex 容器的高度或寬度。

![](https://hackmd.io/_uploads/rJZTxQU4h.png)

2.  `flex-start`：讓 Flex 子元素在交錯軸的起點對齊。

![](https://hackmd.io/_uploads/S11ngQIE3.png)

3.  `flex-end`：讓 Flex 子元素在交錯軸的終點對齊。

![](https://hackmd.io/_uploads/BkwvWmIVn.png)

4.  `center`：讓 Flex 子元素在交錯軸的中心對齊。

![](https://hackmd.io/_uploads/ryiuWX84n.png)

5.  `baseline`：讓 Flex 子元素在文字基線（baseline）對齊。

![](https://hackmd.io/_uploads/HygsWmIN2.png)




這些屬性值可以讓我們靈活地控制 Flex 子元素在交錯軸上的對齊方式，以達到不同的排版效果。例如，使用 `flex-start` 可以將所有 Flex 子元素靠上對齊，而使用 `center` 可以讓它們在交錯軸上置中對齊。


**當我flex-direction轉換，我的交錯軸會更動嗎?**

會的，以下為交錯軸及主軸的方向
![](https://hackmd.io/_uploads/BJlK77IV3.png)
![](https://hackmd.io/_uploads/SJ_9Q7LVh.png)
![](https://hackmd.io/_uploads/ryen77IN2.png)
![](https://hackmd.io/_uploads/SkJamQUNn.png)


## RWD響應式(待整理)

## Practice 履歷表
CodePen:
[A Pen by KazLuo (codepen.io)](https://codepen.io/KazLuo-the-sasster/full/RweMvqB)

index.html:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="css/style.css">
    <title>Document</title>
</head>
<body background="https://i.imgur.com/qQTfOkW.png" class="background"">
    <!--Container-->
    <div class="container">
        <!--intropage 左側分頁-->
        <div class="intropage">
            <div class="tenor-gif-embed" data-postid="17648759" data-share-method="host" data-aspect-ratio="1.17216" data-width="70%"><a href="https://tenor.com/view/cat-cattitude-chat-chattitude-chats-gif-17648759">Cat Cattitude GIF</a>from <a href="https://tenor.com/search/cat-gifs">Cat GIFs</a></div> <script type="text/javascript" async src="https://tenor.com/embed.js"></script>
            <!--Who am i欄位-->
            <h1>Who Am I</h1>
            <h2>駱 揚 季 - 製 程 工 程 師</h2>
            <h3><img src="https://i.imgur.com/44LANHD.png" alt width="20px">&nbsp;連絡電話:0910-041208</h3>
            <h3><img src="https://i.imgur.com/ond4Dcy.png" alt width="20px">&nbsp;電子信箱:<a href="ccc5211@gmail.com">ccc5211@gmail.com</a></h3>
                <h1>About Me</h1>
                <p class="word">碩士期間畢業於國立高雄應用科技大學機械工程學系。
                    在學期間必須獨自面對實驗與理論上的各類變數，使在學期間學習到如何獨自完成實驗與論文的能力，在學期間專於金屬合金的冶煉與材料機械性質上的分析，對於其設備操作及分析具有一定的認知。</p>
            <h1>Hobby</h1>
            <!--Hobby 欄位-->
            <div class="hobby">
                <h4><img src="https://i.imgur.com/fIjfTlp.png" alt="">Game</h4>
                <h4><img src="https://i.imgur.com/O3pvGqA.png" alt="">Read</h4>
                <h4><img src="https://i.imgur.com/QGtRHtm.png" alt="">Tennis</h4>
            </div>   
        </div>         
        <!--mainpage 右側分頁-->
        <div class="mainpage">
        <!--work experience欄位-->
        <h1>Work Experience</h1>
        <p>進入華新科技擔任製程工程師，工作時常需要溝通、協調及即時判斷能力。長久的工作經驗下也具備足夠的抗壓性，與同事間相處融洽。</p>
        <ul>
            <li>2016-2018: 與設備單位合作，一同開發第一套自動化油墨監測系統，直至目前皆已水 
                平展開至各廠區，一年可替公司節省200萬元成本消耗。</li>
            <li>2018-2020:因全球供應趨勢，被動元件供不應求，任職期間為公司提升機台稼動及產能並
                減少原物料消耗。單站生產力&稼動提升20%。</li>
            <li>2021-2023(進行中): 全球物料上漲，委外治具價錢提升。故須提升自製治具能力，降低委
                外治具購買達到節省成本效益。預計一年可節省120萬元</li>
        </ul>
        <!--side project欄位-->
        <h1>Side Project</h1>
        <img src="https://mir-s3-cdn-cf.behance.net/project_modules/max_1200/664638114587787.603f4f3be7779.gif" width="350px" alt="" class="sideproject">
        <p>這是我學習中第一份Prototype專案，遊戲風格採用80年代及Synthwave元素。而遊戲內部Time limit的遊戲手法讓遊戲增添緊張感。遊戲中,你將扮演一顆白色方塊並逃脫永無止境的迷宮。</p>
        </div>
    </div>
</body>
</html>
```
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

/*全區域Border-box */
*, *::before, *::after 
{
    box-sizing: border-box;
}

/*設定圖片響應式*/
img
{
    max-width: 100%;/*設定最大寬度 響應式*/
    height: auto;
    
}

/*設定背景樣式*/
.background
{
    background-size: 600px 600px;
    background-position:50%;
    /*background-position: center;*/
    background-repeat: repeat;
}

/*設定容器*/
.container 
{
  max-width: 1000px;/*設定最大寬度 響應式*/
  display: flex;
  margin: 0 auto;/*置中*/
  justify-content: center;/*置中*/
  margin-top: 10px;
  margin-bottom: 10px;    
}



/*設定左側頁面樣式*/
.intropage
{
    box-shadow: rgba(0, 0, 0, 0.3) 0px 19px 38px, rgba(0, 0, 0, 0.22) 0px 15px 12px;/*設定陰影*/
    background-image: linear-gradient(to right, #204b7c, #3e8ee3);/*設定漸層*/
    text-align: center;
    padding :1.85%;
    width: 50%;
    margin-right: 15px;
    margin-left: 10px;
    border-radius: 30px;/*設定圓角*/
    
}

/*設定左側h1樣式*/
.intropage h1
{
    text-align: start;
    font-family: helvetica;
    font-size: 50px;
    color: azure;
    margin-top: 20px;
    border-bottom: 2px solid azure;
    margin-bottom: 40px;
    padding-bottom: 10px;
    text-indent:0.3em;
}

/*設定左側gif樣式*/
.intropage .tenor-gif-embed
{
    box-shadow: rgba(0, 0, 0, 0.25) 0px 14px 28px, rgba(0, 0, 0, 0.22) 0px 10px 10px;/*設定陰影*/
    width: 200px;
    margin: 0 auto;/*置中*/
    margin-top: 10px;
}

/*設定左側p標籤樣式*/
.intropage p
{
    font-family: Verdana;
    font-size: 20px;
    color: azure;
    padding-left: 50px;
    padding-right: 50px;
    line-height: 30px;
    text-indent:2em;/*設定段落縮排*/
}

/*設定左側p標籤內文樣式*/
.intropage .word
{
    font-family: Verdana;
    font-size: 20px;
    color: azure;
    padding-left: 50px;
    padding-right: 50px;
    line-height: 30px;
    text-indent:2em;
    padding-bottom: 20px;
}

/*設定左側h2標籤樣式*/
.intropage h2
{
    font-family: helvetica;
    margin-top: 5px;
    font-size: 30px;
    color: azure;
    margin-bottom: 20px;
    margin-top: 10px;
}
/*設定左側h3標籤樣式*/
.intropage h3
{
    font-family: Verdana;
    margin-top: 5px;
    font-size: 20px;
    color: azure;
    margin-bottom: 5px;
    margin-top: 10px;
    text-align: center;
}
/*設定左側h4標籤樣式*/
.intropage h4
{
    width: 60px;
    display: flex;
    justify-content: space-evenly;/*設定元素間距*/
    font-family: Verdana;
    margin-top: 5px;
    font-size: 20px;
    color: azure;
    margin-bottom: 5px;
    margin-top: 10px;
  
}

/*設定左側hobby圖片排序樣式*/
.hobby
{
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    margin-bottom: 20px;
}
/*設定左側hobby h4樣式*/
.hobby h4
{
       
    display: flex;
    flex-direction: column;
    /*align-items: center;/*設定將容器中所有元素置中*/
    justify-content: center;/*設定元素置中*/
    text-align: center;

}
/*設定左側hobby h4 img樣式*/
.hobby h4 img {
    margin-bottom: 10px;
  }

  /*設定左側 a標籤樣式*/
.intropage a
{
    font-family: Verdana;
    color: azure;
    text-decoration: none;/*設定無底線*/
}

.intropage a:hover
{
    color: rgb(233, 191, 108);
    text-decoration: underline;/*設定底線*/
}

/*設定左側about me 樣式*/
.aboutme
{
    margin-top: 30px;
}
/*設定左側about me h1樣式*/
.aboutme h1
{
    text-align: start;
    font-family: helvetica;
    font-size: 50px;
    color: azure;
    margin-top: 5px;
    border-bottom: 2px solid azure;
    margin-bottom: 40px;
    text-indent:0.3em; 
    
}


/*設定右側頁面樣式*/
.mainpage
{
    padding :20px;
    width: 50%;
    box-shadow: rgba(0, 0, 0, 0.3) 0px 19px 38px, rgba(0, 0, 0, 0.22) 0px 15px 12px;
    background-image: linear-gradient(to bottom left, #e3e5e7, #ffffff);
    text-align: center;
    border-radius: 30px;
    margin-right: 15px;
    margin-left: 10px;
    
}

/*設定右側 sideproject圖片樣式*/
.mainpage .sideproject
{
    margin-top: 40px;
    box-shadow: rgba(240, 46, 170, 0.4) 5px 5px, rgba(240, 46, 170, 0.3) 10px 10px, rgba(240, 46, 170, 0.2) 15px 15px, rgba(240, 46, 170, 0.1) 20px 20px, rgba(240, 46, 170, 0.05) 25px 25px;

}


/*設定右側 h1標籤樣式*/
.mainpage h1
{
    text-align: start;
    font-family: helvetica;
    font-size: 52px;
    color: rgb(0, 0, 0);
    margin-top: 5px;
    border-bottom: 2px solid rgb(0, 0, 0);
    margin-bottom: 5px;
    padding-bottom: 10px;
    text-indent:0.3em;
}

/*設定右側 ul標籤樣式*/
.mainpage ul
{
    text-align: start;
    margin-top: 20px;
    margin-bottom: 20px;
    list-style-type: disc;
    font-family: helvetica;
    padding-left: 40px;
    padding-right: 40px;
    font-size: 20px;
    color: rgb(0, 0, 0);
    line-height: 30px;
}

/*設定右側 p標籤樣式*/
.mainpage p
{
    text-align: start;
    margin-top: 40px;
    font-family: helvetica;
    font-size: 20px;
    color: rgb(0, 0, 0);
    padding-left: 40px;
    padding-right: 40px;
    line-height: 30px;
    text-indent:2em;/*設定段落縮排*/
}

/*響應式*/
@media only screen and (max-width: 767px) {
    .container {
      flex-direction: column; /* 設定子元素排列方向為垂直排列 */
    }
  
    .intropage, .mainpage {
      width: 95%; /* 在小尺寸螢幕下，讓左右兩側的內容佔據整個容器的寬度 */
      margin-bottom: 20px; /* 在小尺寸螢幕下，讓下頁間距變大 */
      margin-top: 20px;
      
    }
  }
```
