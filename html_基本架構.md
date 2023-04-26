#  html基本架構
###### tags: `html`

```html
<!DOCTYPE html>
<html>
<head>
    <title>這是一個測試頁</title>
</head>
<body>
    <h1>標題</h1>
    <p>這是段落TTTTTTTTEEEESTTTTTTTTTTTTT，</p>
    <p>wjeriljwriwjeir;wje;irj;wiejri;wjeri;</p>
</body>
</html>

```

-   `<!DOCTYPE html>`：告訴瀏覽器這是一個 HTML 文件。
-   `<html>`：整個 HTML 文件的根元素。
-   `<head>`：文件的頭部分，包含了一些 metadata，例如這個文件的標題 (title)。
-   `<title>`：這個 HTML 文件的標題。
-   `<body>`：文件的主要內容區塊，所有要顯示的內容都應該放在這裡。
-   `<h1>`：標題，這個例子中是一個最高級別的標題。
-   `<p>`：段落，這個例子中有兩個段落，分別包含了一些文字。

瀏覽器讀取這個 HTML 文件，根據其中的標籤和內容，顯示出一個網頁。在這個例子中，網頁會顯示一個標題和兩個段落，段落中的內容是 "這是段落TTTTTTTTEEEESTTTTTTTTTTTTT" 和 "wjeriljwriwjeir;wje;irj;wiejri;wjeri;"。

### 補充

**如果不添加<html> </html>是可以的嗎?**

在 HTML5 中， `<html>` 元素是可選的，如果你不添加它，瀏覽器仍然可以顯示網頁內容，因為瀏覽器會自動將缺失的元素補齊。例如，以下是一個不包含 `<html>` 元素的 HTML 5 文件：

```html
<!DOCTYPE html>
<head>
  <title>這是一個測試頁</title>
</head>
<body>
  <h1>標題</h1>
  <p>這是段落TTTTTTTTEEEESTTTTTTTTTTTTT，</p>
  <p>wjeriljwriwjeir;wje;irj;wiejri;wjeri;</p>
</body>
```

在這個例子中，`<html>` 元素被省略了，但瀏覽器仍然可以正確顯示網頁內容。不過，為了確保你的 HTML 文件符合標準，建議還是包含 `<html>` 元素。

**那DocType也可以不需要嗎**

在 HTML 中， `<!DOCTYPE>` 被用來指定 HTML 的版本和文件類型。 `<!DOCTYPE>` 是必需的，如果沒有它，瀏覽器就無法確定正確的文件類型，進而可能導致顯示和解釋錯誤。因此，`<!DOCTYPE>` 是必須的元素，不能省略。

在 HTML5 中， `<!DOCTYPE html>` 是唯一的文件類型聲明，可以放在 HTML 文件的開頭。在 HTML5 中，可以簡化 `<!DOCTYPE>` 的格式，只需要指定 `<!DOCTYPE html>`，而不需要指定 DTD（文檔類型定義）或 URI（統一資源標識符）。

總結來說，`<!DOCTYPE>` 是必需的，不能省略，它指定了 HTML 的版本和文件類型。在 HTML5 中， `<!DOCTYPE html>` 是唯一的文件類型聲明，並且可以簡化格式，不需要指定 DTD 或 URI。

##  Emmet快速建構基本架構

只要在擁有Emmet功能的IDE下皆可快速建構基礎架構
以VScode為例，只要在基礎列打上`!` + `Tab`即可

若需要添加某些標籤(ex.`<p>`標籤需要建構3個，可使用`p*3`
可快速添加三個段落

```html
<!--!+Tab快速生成結構-->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!--這是註解的方式-->
    <!--以下段落使用p*3 + Tab來快速生成3個段落-->
<p></p>
<p></p>
<p></p>
    
</body>
</html>
```

## 如何在網頁中嵌入圖檔

在`<body>`階層中加入`img` + `Tab`產生架構
並在`src`的部分裝入與html同資料夾的圖檔，即可插入

- `<img>` 標籤用於添加圖像，`src` 屬性指定圖像的 URL，`alt` 屬性為圖像添加一個替代文字描述，當圖像無法顯示時，替代文字會顯示在網頁上。在這個例子中，`alt` 屬性設置為「鯊魚翻頁」，當圖像無法顯示時，就會顯示這段文字。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>這是測試頁面</title>
</head>
<body>
    <!--這是註解的方式-->
    
    <h1>這是標題</h1>
<p>J是段落</p>
<p>UIQJEQWOIJEQOIEJQWIO</p>
<p>jeqilejqiljeqiljeilqwejql</p>
    <!--添加圖檔的方式打上img + Tab產生結構，並將同層資料夾內的檔案名稱置入-->

<!--在與htlm同層資料夾可直接輸入檔名-->    
<img src="1_9-Il_nJ8_lgeJreXTkxLsw.gif" alt="鯊魚翻頁">
<!--在與htlm同層資料夾內的資料夾內的檔案，則需輸入資料夾名稱/檔名-->
<img src="img/logo_gmail_lockup_dark_2x_r5.png" alt="Gmail LOGO">
<!--若是外部資料，則可以直接輸入其網址-->
<img src="https://www.udemy.com/staticx/udemy/images/v7/logo-udemy.svg" alt="Udemy LOGO">
    
</body>
</html>
</html>
```
完成後:
![](https://hackmd.io/_uploads/H1r1kD8mn.png)


這邊針對`meta`標籤做一下補充，meta類似於屬性的添加，用於提供有關文檔的元數據（metadata），例如頁面的描述、作者、關鍵字等。`<meta>` 元素中的屬性（例如 `charset`、`http-equiv`、`name`、`content` 等）可以用來指定文檔的編碼方式、重定向網頁、設置視口大小等。`<meta>` 元素中的屬性對網站的搜索引擎優化（SEO）也非常重要。因此，`<meta>` 元素通常用於在不可見的方式提供有關文檔的信息，而不會對頁面的外觀或交互造成影響。

-   `<meta charset="UTF-8">` 設置了頁面使用的字符集為 UTF-8。
    
-   `<meta http-equiv="X-UA-Compatible" content="IE=edge">` 告訴瀏覽器使用最新的渲染模式。
    
-   `<meta name="viewport" content="width=device-width, initial-scale=1.0">` 用於定義頁面的視口，以便在不同設備上呈現適當的大小。

**meta通常都只放置於head標籤嗎**

是的，`<meta>` 元素通常被放置在 `<head>` 元素內，用於提供有關文檔的元數據（metadata），例如頁面的描述、作者、關鍵字等。`<meta>` 元素中的屬性（例如 `charset`、`http-equiv`、`name`、`content` 等）可以用來指定文檔的編碼方式、重定向網頁、設置視口大小等。`<meta>` 元素中的屬性對網站的搜索引擎優化（SEO）也非常重要。因此，`<meta>` 元素通常用於在不可見的方式提供有關文檔的信息，而不會對頁面的外觀或交互造成影響。

## 如何在網頁中加上連結(標籤`<a>`)

網頁中添加超連結在`<body>`標籤中加入`<a herf="網址"> 提示字元 <a>` 即可以下為範例，其中我添加了yahoo及google的連結至網頁內
並在後面分別寫上"這是yahoo/google連結"以示標記

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>這是測試頁面</title>
</head>
<body>
    <!--這是註解的方式-->
    <!--以下段落使用p*3 + Tab來快速生成3個段落-->
    <h1>這是標題</h1>
    <!--輸入a herf 並輸入網址及其提示字元-->
    <a href = "https://www.yahoo.com">這是yahoo連結</a>
    <!--若在網址後面添加 target = "_blank"則點擊網址後往只會開出新分頁-->
    <!--若在網址後面添加title = " " 則在滑鼠游標移過去時顯示提示字元-->
    <a href="https://www.google.com" target="_blank" title = "是沒看過逆">這是google連結</a>
    
<p>J是段落</p>
<p>UIQJEQWOIJEQOIEJQWIO</p>
<p>jeqilejqiljeqiljeilqwejql</p>
    <!--添加圖檔的方式打上img + Tab產生結構，並將同層資料夾內的檔案名稱置入-->

<!--在與htlm同層資料夾可直接輸入檔名-->    
<img src="1_9-Il_nJ8_lgeJreXTkxLsw.gif" alt="鯊魚翻頁">
<!--在與htlm同層資料夾內的資料夾內的檔案，則需輸入資料夾名稱/檔名-->
<img src="img/logo_gmail_lockup_dark_2x_r5.png" alt="Gmail LOGO">
<!--若是外部資料，則可以直接輸入其網址-->
<img src="https://www.udemy.com/staticx/udemy/images/v7/logo-udemy.svg" alt="Udemy LOGO">
    
</body>
</html>
```
- `target = _blank`:加上這段則點開後的網址會以開新分頁的方式呈現，而不是直接移動至該網址
- `title = " "`:加上這段可在滑鼠移動至連結時產生提示字元
![](https://hackmd.io/_uploads/B1cU08873.png)

### 補充

這邊可以探討一下標籤`<a></a>`
通常在前段`<a>`中可以添加相對應屬性來對a標籤做制定

像是:

`<a href ="https://ww.google.com" title="gooooogle">google page</a>`
其中就添加了`href`及 `title`屬性

`<a></a>`標籤很常應用在網頁設計，常見就像新聞頁面中會在內文(p段落標籤)中添加連結，算是很常使用的標籤種類



## `<ul> <li>`標籤

`<ul>``<li>`標籤在網頁中隨處可見，使用在網頁的條列式選項
並以`<ul>`作為外框，而`<li>`則為內部選項
![](https://hackmd.io/_uploads/rkox9w8X2.png)

以下為基礎範例:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>這是測試頁面</title>
</head>
<body>
    <h1>這是標題</h1>
    <!--輸入a herf 並輸入網址及其提示字元-->
    <a href = "https://www.yahoo.com">這是yahoo連結</a>
    <!--若在網址後面添加 target = "_blank"則點擊網址後往只會開出新分頁-->
    <!--若在網址後面添加title = " " 則在滑鼠游標移過去時顯示提示字元-->
    <a href="https://www.google.com" target="_blank" title = "是沒看過逆">這是google連結</a>

    <!--添加圖檔的方式打上img + Tab產生結構，並將同層資料夾內的檔案名稱置入-->
<!--在與htlm同層資料夾可直接輸入檔名-->    
<img src="1_9-Il_nJ8_lgeJreXTkxLsw.gif" alt="鯊魚翻頁">
<!--在與htlm同層資料夾內的資料夾內的檔案，則需輸入資料夾名稱/檔名-->
<img src="img/logo_gmail_lockup_dark_2x_r5.png" alt="Gmail LOGO">
<!--若是外部資料，則可以直接輸入其網址-->
<img src="https://www.udemy.com/staticx/udemy/images/v7/logo-udemy.svg" alt="Udemy LOGO">

<!--在ul外殼中添加li標籤來新增項目，可產生條列式效果-->
<ul>    
    <li>項目1</li>
    <li>項目2</li>
    <li>項目3</li>
</ul>
<!--若想要將標記改為數字，則使用ol-->
<ol>
    <li>項目1</li>
    <li>項目2</li>
    <li>項目3</li>
</ol>
    
</body>
</html>
```

效果如下
![]([https://hackmd.io/_uploads/SJmGoPLQ3.png](https://hackmd-prod-images.s3-ap-northeast-1.amazonaws.com/uploads/upload_775ca7bd979ee91999a7d2c7e48561c4.png?AWSAccessKeyId=AKIA3XSAAW6AWSKNINWO&Expires=1682500949&Signature=9g6P7zVnjwOMToRoNnku57KGLiE%3D))







