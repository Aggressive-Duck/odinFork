### 介紹

所有的HTML文件都有相同的基本結構或樣板，這些需要在做任何有用的事情之前就位。在本課中，我們將探討這些樣板的不同部分，並看看它們如何組合在一起。

### 課程概述

本節包含您將在本課中學習的主題的一般概述。

- 如何編寫HTML文件的基本樣板。
- 如何在瀏覽器中打開HTML文件。

### 創建HTML文件

為了演示HTML樣板，我們首先需要一個HTML文件來操作。

在您的電腦上創建一個新文件夾，並將其命名為`html-boilerplate`。在該文件夾內創建一個新文件，並將其命名為`index.html`。

您可能已經熟悉許多不同類型的文件，例如doc、pdf和圖像文件。

為了讓電腦知道我們要創建一個HTML文件，我們需要在文件名後加上`.html`擴展名，就像我們在創建`index.html`文件時所做的那樣。

值得注意的是，我們將HTML文件命名為`index`。我們應該始終將包含我們網站首頁的HTML文件命名為`index.html`。這是因為當用戶訪問我們的網站時，網絡服務器會默認查找`index.html`頁面——沒有它會導致大問題。

### DOCTYPE

每個HTML頁面都以doctype聲明開始。doctype的目的是告訴瀏覽器應該使用哪個版本的HTML來渲染文檔。最新版本的HTML是HTML5，該版本的doctype是`<!DOCTYPE html>`。

舊版本HTML的doctype有點複雜。例如，這是HTML4的doctype聲明：

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
```
然而，我們可能永遠不會想要使用舊版本的HTML，所以我們將始終使用<!DOCTYPE html>。

在您的文本編輯器中打開之前創建的index.html文件，並將<!DOCTYPE html>添加到第一行。

### HTML元素
在我們聲明doctype之後，我們需要提供一個<html>元素。這就是所謂的文檔的根元素，這意味著文檔中的每個其他元素都將是它的後代。

當我們學習使用JavaScript操作HTML時，這變得更加重要。目前，只需知道<html>元素應包含在每個HTML文檔中。

回到index.html文件，讓我們通過輸入其開放和閉合標籤來添加<html>元素，如下所示：
```html
<!DOCTYPE html>
<html lang="en">
</html>
```

注意到這裡的lang這個詞了嗎？它代表與給定HTML標籤（即<html>）相關聯的HTML屬性。這些屬性提供有關HTML元素的附加信息。（更多關於HTML屬性的內容在後面的課程中。）

#### lang屬性是什麼？
`lang`指定該元素中文本內容的語言。此屬性主要用於提高網頁的可訪問性。它允許輔助技術，例如屏幕閱讀器，根據語言進行調整並調用正確的發音。

### Head元素

`<head>` 元素是我們放置有關我們網頁的重要元信息以及網頁在瀏覽器中正確渲染所需的內容的地方。
在 `<head>` 內，我們**不應該**使用任何在網頁上顯示內容的元素。

回到我們的 `index.html` 文件，讓我們在其中添加一個包含 `<meta>` 元素和標題的 `<head>` 元素。
`<head>` 元素位於 `<html>` 元素內，應始終是開放 `<html>` 標籤下的第一個元素：
```html
<!DOCTYPE html>

<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>My First Webpage</title>
  </head>
</html>
```
#### Meta元素
我們應該始終在<head>元素中包含帶有網頁字符集編碼的<meta>標籤：<meta charset="utf-8">。

設置編碼非常重要，因為它確保網頁能夠在瀏覽器中正確顯示來自不同語言的特殊符號和字符。

#### Title元素
我們應該始終在HTML文檔的head中包含的另一個元素是`<title>`元素：

`<title>我的第一個網頁</title>`

<title>元素用於為網頁提供人類可讀的標題，該標題顯示在我們網頁的瀏覽器標籤中。例如，如果您查看當前瀏覽器標籤的名稱，它將顯示“HTML Boilerplate &#124; | The Odin Project”；這是當前.html文件的<title>。

如果我們不包含<title>元素，網頁的標題將默認為其文件名。在我們的例子中，這將是index.html，這對用戶來說沒有什麼意義；如果用戶打開了許多瀏覽器標籤，這將使他們很難找到我們的網頁。

HTML文檔的head中可以包含更多元素。然而，目前只需要了解我們在這裡介紹的兩個元素。我們將在整個課程中介紹更多進入head的元素。

### Body元素
完成HTML樣板所需的最後一個元素是`<body>`元素。這是所有將顯示給用戶的內容所在的位置——文本、圖片、列表、鏈接等。

要完成樣板，請將`<body>`元素添加到index.html文件中。`<body>`元素也位於`<html>`元素內，並且始終位於`<head>`元素下方，如下所示：
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>My First Webpage</title>
  </head>

  <body>
  </body>
</html>
```
### 在瀏覽器中查看HTML文件
此時，`index.html`文件中的HTML樣板已完成，但如何在瀏覽器中查看它呢？有幾種不同的選擇：

<div class="lesson-note lesson-note--warning" markdown="1">

#### 使用Google Chrome

為了避免分支我們的課程說明以適應瀏覽器之間的所有差異，我們將使用Google Chrome作為本課程其餘部分的主要瀏覽器。所有對瀏覽器的引用都將特別針對Google Chrome。我們**強烈**建議您在今後的所有測試中使用Google Chrome。

</div>

1. 您可以將HTML文件從文本編輯器拖放到瀏覽器的地址欄中。

1. 您可以在文件系統中找到HTML文件，然後雙擊它。這將在系統使用的默認瀏覽器中打開該文件。

1. 您可以使用終端在瀏覽器中打開該文件：
   - Ubuntu：導航到包含該文件的目錄並輸入`google-chrome index.html`
   - macOS：導航到包含該文件的目錄並輸入`open ./index.html`
   - WSL：導航到包含該文件的目錄並輸入`explorer.exe index.html`。請注意，這將在系統使用的默認瀏覽器中打開該文件。
  使用上述方法之一，打開我們一直在處理的`index.html`文件。您會注意到屏幕是空白的。這是因為我們的body中沒有任何顯示的內容。

回到`index.html`文件，讓我們在body中添加一個標題（稍後會詳細介紹），並保存文件：

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>My First Webpage</title>
  </head>

  <body>
    <h1>Hello World!</h1>
  </body>
</html>
```

現在，如果您刷新瀏覽器中的頁面，您應該會看到更改生效，並顯示標題“Hello World！”。

### VSCode快捷方式
VSCode有一個內置的快捷方式，您可以用來一次生成所有樣板。請注意，此快捷方式僅在編輯具有`.html`擴展名的文件或已選擇HTML語言的文本文件時有效。要觸發快捷方式，刪除`index.html`文件中的所有內容，然後在第一行輸入`!`。這將彈出幾個選項。按<kbd>Enter</kbd>鍵選擇第一個選項，瞧，您應該會看到所有樣板都為您填充好了。

您可能會注意到此快捷方式生成的樣板包含一行我們尚未提到的內容：

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

這不是我們需要了解的內容，直到我們討論響應式設計，這是一個涉及不同屏幕尺寸的高級主題，我們將在課程的後面部分介紹。目前，您可以將該行保留原樣。

知道如何自己編寫樣板仍然是很好的，以防您發現自己使用像記事本這樣的文本編輯器（天哪），它沒有這個快捷方式。在您的前幾個HTML項目中，盡量不要使用快捷方式，這樣您可以為編寫樣板代碼建立一些肌肉記憶。

### 作業
<div class="lesson-content__panel" markdown="1">

1. 觀看並跟隨Kevin Powell的精彩構建您的第一個網頁視頻。 [建立你第一個網站影片](https://www.youtube.com/watch?v=V8UAEoOvqFg&t=93s).

1. 通過刪除`index.html`文件的內容並嘗試從記憶中再次寫出所有樣板來建立一些肌肉記憶。如果您卡住了，不要擔心，如果您需要偷看課程內容前幾次。只要繼續，直到您能夠從記憶中做幾次。

1. 通過W3 HTML驗證器運行您的樣板。[HTML validator](https://validator.w3.org/#validate_by_input). 驗證器確保您的標記是正確的，是一個很好的學習工具，因為它們提供有關您可能經常犯的語法錯誤的反饋，而您可能不知道，例如缺少閉合標籤和HTML中的額外空格。

</div>

### 知識檢查
以下問題是反思本課中關鍵主題的機會。如果您無法回答某個問題，請點擊它以查看相關材料，但請記住，您不需要記住或掌握這些知識。

doctype聲明的目的是什麼？
HTML元素是什麼？
head元素的目的是什麼？
body元素的目的是什麼？
### 其他資源
本節包含與相關內容的有用鏈接。這不是必需的，因此請將其視為補充材料。

另一個在瀏覽器中打開HTML頁面的選項是使用VSCode的Live Preview擴展。這將打開您的HTML文檔，並在每次保存文檔時自動刷新它。然而，我們建議不要使用這個擴展，而是用傳統的方式，在您的前幾個HTML項目中手動打開頁面並刷新頁面。這樣，您可以習慣這個過程，而不會立即依賴擴展。

如果您願意，您可以將lang屬性添加到整個網頁的各個元素中。