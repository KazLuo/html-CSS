# CSS-基礎

###### tags: `CSS`

## CSS和HTML差異在哪?

CSS和HTML是構建網頁的兩個基本技術。雖然它們經常一起使用，但它們的目的和功能是不同的。

HTML（超文本標記語言）是一種用於創建網頁內容和結構的標記語言。HTML用於定義網頁的結構，例如標題、段落、圖像、列表等。它提供了一種組織和顯示網頁內容的方法。

CSS（層疊樣式表）是一種用於描述網頁外觀和樣式的樣式語言。它用於設置網頁的佈局、顏色、字體、大小和其他外觀屬性。通過使用CSS，可以輕鬆地控制網頁的外觀，而不需要修改HTML內容。

總的來說，HTML定義網頁的結構和內容，而CSS定義網頁的外觀和樣式。它們一起工作，使網頁的設計和呈現更加靈活和易於管理。


## 基礎框架建立及改變字體大小/顏色/位置

1. 首先創立一個"index.html"並建立

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!--輸入 link + Tab 生成連結css的架構-->
    <!-- 另外在VScode中新增一份style.css檔案在同資料夾中-->
    <link rel="stylesheet" href="style.css">
    <title>Document</title>
</head>
<body>
    <!--添加一個標題-->
    <h1>這是一個標題</h1>    
    
</body>
</html>
```

2. 其中在`<body>`標籤中使用`<h1>`生成標題，並在`<head>`標籤中輸入`link` + `Tab`生成插入css基礎架構

3. 接著使用VScode生成一個新文件"style.css"並輸入以下程式碼

```css
h1 
{
    color :brown;
    font-size: 50px;
    text-align: center;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}
```

這邊補充說明:
這段CSS定義了標題(h1)的樣式：

-   `color: brown;` 指定文字的顏色為棕色。
-   `font-size: 50px;` 設定文字的大小為50像素。
-   `text-align: center;` 將文字置中對齊。
-   `font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;` 定義使用的字體，從左至右優先使用'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS'，如果都沒有的話就使用預設的sans-serif字體。

總結來說，這段CSS將標題的文字設定為棕色、50像素大小、置中對齊，並且使用了優先級別高的字體。

關於`font-family`查了一下

![](https://hackmd.io/_uploads/B1ANFOI7n.png)
這段是CSS font-family屬性的說明，表示font-family屬性可以用來定義一個優先級別的字體族群清單，其中可以列出具體的字體名稱或通用字體名稱。當使用者代理（例如瀏覽器）需要渲染一個字元時，它會遍歷這個字體族群清單，直到找到一個可以渲染這個字元的字體為止。

`<family-name>`則是指用來定義字體名稱的值，可以是具體的字體名稱，如`Arial`或`Times New Roman`，也可以是通用字體名稱，如`serif`、`sans-serif`、`monospace`等。如果優先級別高的字體不可用，使用者代理會選擇下一個字體。通常會在清單的最後面指定一個通用字體名稱，以作為回落字體，即當沒有其他字體可用時，使用者代理會使用此字體。

簡單來說，瀏覽器會依照`font-family`中定義的字體從頭到尾進行測試如果第一個字體支援則使用第一個，若不刑則測試第二個...以此類推



