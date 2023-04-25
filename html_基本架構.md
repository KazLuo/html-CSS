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

## 補充

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
    <!--使用!+Tab快速生成機html架構-->
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


