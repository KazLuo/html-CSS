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

**css的格式架構:**
```
選擇器
{
    屬性:設定值;
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

**如何確定自己有成功套用css樣式?**
對頁面右鍵點出"檢查"按鈕並開啟開發者工具

![](https://hackmd.io/_uploads/S17LgjDQn.png)

從開發者工具中可以看見左側的html及右側套用了什麼css樣式
例如上圖我點選標題的部分，css正確顯示出我所輸入的屬性，假如css格式錯誤或是其他異常造成css樣式無法植入，開發者工具也會顯示出來

![](https://hackmd.io/_uploads/H1nzWjPQn.png)

以上為因為輸入錯字
造成css屬性無法植入，當然還有許多原因會造成無法植入，像是缺少`;` `{}`等字符

## 標籤選擇器

剛才所提到css基礎架構中有一個"選擇器"，而這個選擇器則是控制html中
對應的各項，一開始我們接觸到的選擇器為"標籤選擇器"其用法是直接在選擇器端打上html相對應標籤達到修改其屬性的效果。

```css
h1 /*標籤選擇器*/
{
    color :brown;
    font-size: 50px;
    text-align: center;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}
```

以下為範例:

index.html:

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
    <p>段落</p>
    <a href="https://www.udemy.com/">udemy</a>
    <ul>
        <li>項目1</li>
        <li>項目2</li>
        <li>項目3</li>
    </ul>
    
</body>
</html>
```
style.css:

```css
h1 
{
    color :brown;
    font-size: 50px;
    text-align: center;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}
p
{
    color : blue;
    font-size: 50px;
    text-align: right;
}
a
{
    color : rgb(255, 0, 255);
    font-size: 50px;
    text-align: center;
}
ul
{
    color : rgb(255, 115, 0);
    font-size: 50px;
    text-align: center;

}

}
```
最終效果:
![](https://hackmd.io/_uploads/Syro4iwXn.png)

標籤選擇器雖然使用上十分簡單，但是他卻因為綁定標籤修改屬性的特性
造成若多行標籤需要有不同設定就會無法實現，因此會需要其他選擇器來達成效果。

## 擬態選擇器(hover active)

在 CSS 中，擬態選擇器（Pseudo-selectors）是用於選取元素的特定狀態或位置的選擇器。它們以冒號（:）開頭，並添加到選擇器的末尾，以指定要選擇的元素的特定狀態。

以下是一些常用的擬態選擇器：

1.  :hover - 選取鼠標懸停在元素上的狀態。
2.  :active - 選取元素被激活（按下）的狀態。
3.  :focus - 選取獲得焦點的元素。
4.  :visited - 選取已被訪問過的連結的狀態。
5.  :first-child - 選取作為父元素的第一個子元素的元素。
6.  :last-child - 選取作為父元素的最後一個子元素的元素。
7.  :nth-child() - 選取作為父元素的特定子元素的元素，可以使用表達式指定要選擇的子元素。

這些擬態選擇器可以與元素選擇器結合使用，以便針對元素的特定狀態應用樣式。這樣可以根據使用者的操作

這邊簡單的示範較常使用的hover及active選擇器

hover本身較常使用在連結上 css樣式如下:

```css
h1 
{
    color :brown;
    font-size: 50px;
    text-align: center;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}
h1 
{
    color :brown;
    font-size: 50px;
    text-align: center;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}
p
{
    color : blue;
    font-size: 50px;
    text-align: right;
}
a/*原始連結的樣式*/
{
    color : rgb(255, 0, 255);
    font-size: 50px;
    text-align: center;
}
a:hover/*滑鼠移過連結的樣式*/
{
    color : rgb(255, 0, 0);
    font-size: 70px;
    text-align: center;
}

a:active/*點擊(下壓)連結的樣式*/
{
    color : rgb(0, 255, 21);
    font-size: 50px;
    text-align: center;
}

ul
{
    color : rgb(255, 115, 0);
    font-size: 30px;
    text-align: center;

}

}
```
a標籤原始樣式:

![](https://hackmd.io/_uploads/H1IrhjDQ3.png)


a:hover
滑鼠移過連結:
- 字體變紅
- 字體大小由50 &rarr; 70 px

![](https://hackmd.io/_uploads/rk0XjjD72.png)

a:active
點擊連結:
- 字體變綠
- 字體大小由50 &rarr; 30 px

![](https://hackmd.io/_uploads/rJc1njvXh.png)

## 類別選擇器

剛才在標籤選擇器有提到，若針對多種同類標籤進行多類型修改使用標籤選擇器是無法達成的，因此需要*類別選擇器*來針對同標籤進行多種css樣式植入

以下為範例:

index.html:

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
 
    <ul>
        <li>項目1</li>
        <li class="radStyle">項目2</li><!--使用css中redStyle之類別選擇器-->
        <li class="blueStyle">項目3</li><!--使用css中blueStyle之類別選擇器-->
        <li class="greenStyle">項目4</li><!--使用css中greenStyle之類別選擇器-->
        <li class="pinkStyle">項目5</li><!--使用css中pinkStyle之類別選擇器-->
    
</body>
</html>
```

style.css:

```css
ul /*標籤選擇器*/
{
    color:aqua;

}
.radStyle /*類別選擇器*/
{
    color:red;
}
.greenStyle /*類別選擇器*/
{
    color:green;
}
.blueStyle /*類別選擇器*/
{
    color:blue;
}
.pinkStyle /*類別選擇器*/
{
    color:pink;
}


```
在html頁面須注意若要套用類別選擇器的樣式，需添加`class="列別選擇器"`，而在css樣式中若要創建類別選擇器，須注意在開頭要加上`.`才可以正常創建類別選擇器

## 常見排版優化屬性

若想在某些html標籤中添加不規則字樣來測試效果，可以輸入`lorem`+字數來創建出假文字。

以下為範例:

index.cs:
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
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloribus voluptate quia beatae, iste, distinctio velit incidunt consectetur deserunt, adipisci dicta porro dolores ipsum consequuntur? Doloribus distinctio quasi at reiciendis qui!</p>
<!--上面使用lorem30-->
</body>
</html>
```
![](https://hackmd.io/_uploads/rJ0uvnP7h.png)

常見排版優化:
style.css:

```css
p
{
    font-family: Arial, Helvetica, sans-serif;/*字體*/
    font-size: 20px;/*字體大小*/
    line-height: 1.5;/*1.5倍行高,也可使用px*/
    text-align: left;/*文字對齊*/
    text-indent: 50px;/*文字縮排*/
    letter-spacing: 2px;/*字間距*/
    text-decoration: underline;/*文字裝飾*/

}
```



效果如下:
![](https://hackmd.io/_uploads/rJqy2hDm3.png)



## 在html中添加線條

時常在網頁中常會看見線條區分網頁，通常這部分會使用css中的`border`來實現線條效果，若是使用圖片可能會影響效能。

在 CSS 的 `border` 屬性中，您可以指定不同的線條樣式。以下是一些常見的線條樣式值：

1.  `none`：無線條。
2.  `solid`：實線。
3.  `dashed`：虛線，由短橫線和短間隔交替組成。
4.  `dotted`：點線，由小圓點組成。
5.  `double`：雙線，由兩條平行的線組成。
6.  `groove`：3D凹槽效果，看起來像是凹陷的線條。
7.  `ridge`：3D脊線效果，看起來像是凸起的線條。
8.  `inset`：3D內凹效果，看起來像是向內的線條。
9.  `outset`：3D外凸效果，看起來像是向外的線條。

這些線條樣式可以應用在 `border` 屬性中的不同邊框（top、right、bottom、left）上，也可以使用縮寫形式一次性指定多個邊框的樣式。

以下為範例:

index.html

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
    <img src="logo_gmail_lockup_dark_2x_r5.png" alt="gmail">
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloribus voluptate quia beatae, iste, distinctio velit incidunt consectetur deserunt, adipisci dicta porro dolores ipsum consequuntur? Doloribus distinctio quasi at reiciendis qui!</p>
    <a href="#">TEST</a>
</body>
</html>
```

style.css:

```css
p
{
    font-family: Arial, Helvetica, sans-serif;/*字體*/
    font-size: 20px;/*字體大小*/
    line-height: 1.5;/*1.5倍行高,也可使用px*/
    text-align: left;/*文字對齊*/
    text-indent: 50px;/*文字縮排*/
    letter-spacing: 2px;/*字間距*/
    text-decoration: underline;/*文字裝飾*/
    border: 2px solid black;/*若單純border則為邊框*/

}

img
{
    /*以下展示不同線條效果*/
    border-left: 10px dashed blue;/*左邊框*/
    border-right: 10px dotted green ;/*右邊框*/
    border-top: 10px double red; /*上邊框*/
    border-bottom: 10px solid orange ;/*下邊框*/
}

a
{
    border-left: 10px groove blue;/*左邊框*/
    border-right: 10px ridge green ;/*右邊框*/
    border-top: 10px inset red; /*上邊框*/
    border-bottom: 10px outset orange ;/*下邊框*/

}
```
顯示效果:
![](https://hackmd.io/_uploads/HkiJrawmn.png)


