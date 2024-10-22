### 介紹

所有的 HTML 文件都有相同的基本結構或模板，這些在開始進行任何有用的工作之前必須先設定好。在這堂課中，我們將探索這些模板的不同部分，並了解它們如何整合在一起。

### 課程概述

此部分包含你將在本課中學習的主題概述。

- 如何撰寫 HTML 文件的基本模板。
- 如何在瀏覽器中打開 HTML 文件。

### 建立 HTML 檔案

為了演示 HTML 的模板，我們首先需要一個 HTML 文件來進行操作。

在你的電腦上建立一個新資料夾，命名為 `html-boilerplate`。在該資料夾內建立一個新文件，命名為 `index.html`。

你可能已經熟悉許多不同類型的文件，例如 doc、pdf 和圖片文件。

為了讓電腦知道我們想要建立一個 HTML 文件，我們需要在文件名稱後加上 `.html` 擴展名，就像我們在創建 `index.html` 文件時所做的那樣。

值得注意的是，我們將 HTML 文件命名為 `index`。我們應該始終將包含我們網站首頁的 HTML 文件命名為 `index.html`。這是因為當用戶訪問我們的網站時，網頁伺服器會預設尋找 `index.html` 頁面——如果沒有該頁面，將會導致問題。

### DOCTYPE

每個 HTML 頁面都以 doctype 宣告開始。doctype 的目的是告訴瀏覽器應該使用哪個版本的 HTML 來呈現文件。最新版本的 HTML 是 HTML5，其 doctype 宣告為 `<!DOCTYPE html>`。

舊版本的 HTML 的 doctype 宣告要複雜一些。例如，這是 HTML4 的 doctype 宣告：

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
```

然而，我們可能永遠不會使用舊版本的 HTML，因此我們將始終使用 `<!DOCTYPE html>`。

打開我們之前在文本編輯器中創建的 `index.html` 文件，並在第一行添加 `<!DOCTYPE html>`。

### HTML 元素

宣告完 doctype 之後，我們需要提供一個 `<html>` 元素。這是文件的根元素，這意味著文件中的所有其他元素都將是它的子元素。

這在後來我們學習使用 JavaScript 操作 HTML 時會變得更加重要。現在只需知道每個 HTML 文件中都應該包含 `<html>` 元素。

回到 `index.html` 文件中，讓我們通過輸入其開頭和結尾標籤來添加 `<html>` 元素，如下所示：

```html
<!DOCTYPE html>
<html lang="en">
</html>
```

注意這裡的 `lang` 是什麼？它代表與給定 HTML 標籤（即此例中的 `<html>`）相關的 HTML 屬性。這些屬性提供有關 HTML 元素的附加信息。（更多關於 HTML 屬性的內容會在下一課中介紹。）

#### lang 屬性是什麼？

`lang` 指定該元素中文本內容的語言。這個屬性主要用於提高網頁的可訪問性。它允許輔助技術（例如螢幕閱讀器）根據語言進行適應，並調用正確的發音。

### Head 元素

`<head>` 元素是我們放置有關網頁的重要元信息以及網頁在瀏覽器中正確呈現所需內容的地方。
在 `<head>` 中，我們**不應該**使用任何會在網頁上顯示內容的元素。

回到我們的 `index.html` 文件，讓我們在 `<html>` 元素內添加一個 `<head>` 元素，並在其中包含 `<meta>` 元素和標題。`<head>` 元素應位於 `<html>` 標籤下的第一個元素：

```html
<!DOCTYPE html>

<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>My First Webpage</title>
  </head>
</html>
```

#### Meta 元素

我們應該始終在 `<head>` 元素中包含一個使用字符集編碼的 `<meta>` 標籤：`<meta charset="UTF-8">`。

設置編碼非常重要，因為它確保網頁可以正確顯示不同語言中的特殊符號和字符。

#### Title 元素

另一個應該始終包含在 HTML 文件 `<head>` 中的元素是 `<title>` 元素：

```html
<title>My First Webpage</title>
```

`<title>` 元素用於為網頁提供一個人類可讀的標題，該標題將顯示在我們網頁的瀏覽器標籤中。例如，如果你查看當前瀏覽器標籤的名稱，它會顯示 "HTML Boilerplate &#124; The Odin Project"；這就是當前 `.html` 文件的 `<title>`。

如果我們沒有包含 `<title>` 元素，網頁的標題將默認為其文件名。在我們的例子中，這將是 `index.html`，這對用戶來說並不太有意義；如果用戶打開了許多瀏覽器標籤，將會難以找到我們的網頁。

HTML 文件 `<head>` 中還可以包含許多其他元素。然而，現在你只需了解我們在這裡介紹的這兩個元素即可。我們將在後面的課程中介紹更多適合放入 `<head>` 的元素。

### Body 元素

要完成 HTML 模板，最後需要的元素是 `<body>` 元素。這是放置將向用戶顯示的所有內容的地方，包括文本、圖片、列表、鏈接等。

要完成模板，將 `<body>` 元素添加到 `index.html` 文件中。`<body>` 元素應位於 `<html>` 元素內，並且總是位於 `<head>` 元素的下方，如下所示：

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

### 在瀏覽器中查看 HTML 文件

此時，`index.html` 文件中的 HTML 模板已完成，但如何在瀏覽器中查看呢？有幾種不同的方法：

<div class="lesson-note lesson-note--warning" markdown="1">

#### 使用 Google Chrome

為了避免分支課程指令來適應不同瀏覽器之間的差異，我們將使用 Google Chrome 作為本課程其餘部分的主要瀏覽器。所有與瀏覽器相關的參考都將專門針對 Google Chrome。我們**強烈建議**你使用 Google Chrome 進行所有測試。

</div>

1. 你可以將 HTML 文件從文本編輯器拖放到瀏覽器的地址欄中。

1. 你可以在文件系統中找到該 HTML 文件，然後雙擊它。這將在系統使用的默認瀏覽器中打開該文件。

1. 你可以使用終端打開該文件：
   - Ubuntu：導航至包含文件的目錄，輸入 `google-chrome index.html`
   - macOS：導航至包含文件的目錄，輸入 `open ./index.html`
   - WSL：導航至包含文件的目錄，輸入 `explorer.exe index.html`。注意，這將在系統使用的默認瀏覽器中打開該文件。

使用上述方法之一打開我們剛才編輯的 `index.html` 文件。你會注意到螢幕是空白的。這是因為我們的 body 中還沒有任何顯示的內容。

回到 `index.html` 文件中，讓我們在 body 中添加一個標題（稍後會詳細介紹），並保存該文件：

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

現在，如果你刷新瀏覽器中的頁面，你應該會看到頁面顯示了 "Hello World!" 標題。

### VSCode 快捷鍵

VSCode 有一個內建的快捷鍵，可以一鍵生成所有模板。請注意，此快捷鍵僅在編輯 `.html` 擴展名的文件或已選擇 HTML 語言的文本文件時有效。要觸發此快捷鍵，請刪除 `index.html` 文件中的所有內容，然後在第一行輸入 `!`。這將彈

出幾個選項。按 <kbd>Enter</kbd> 鍵選擇第一個選項，瞧，你應該會看到所有的模板已經自動生成。

你可能會注意到該快捷鍵生成的模板中包含一行我們尚未提到的代碼：

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

這個元素我們暫時不需要知道，直到我們討論響應式設計（這是一個涉及不同屏幕尺寸的高級主題），我們會在課程的後面介紹。現在，你可以保留這一行。

不過，學會自己撰寫模板依然是很重要的，以防你使用的文本編輯器（比如 notepad）沒有這個快捷鍵。在你完成最初幾個 HTML 專案時，盡量不要使用這個快捷鍵，以便為撰寫模板代碼建立一些肌肉記憶。

### 作業

<div class="lesson-content__panel" markdown="1">

1. 觀看並跟隨 Kevin Powell 的精彩視頻 [Building Your First Web Page video](https://www.youtube.com/watch?v=V8UAEoOvqFg&t=93s)。

1. 通過刪除 `index.html` 文件的內容並嘗試從記憶中重新撰寫所有模板來建立肌肉記憶。如果你第一次卡住了，不要擔心偷看課程內容。只需不斷嘗試，直到你能夠幾次從記憶中完成它。

1. 將你的模板通過 W3 [HTML 驗證器](https://validator.w3.org/#validate_by_input) 進行驗證。驗證器確保你的標記語法正確，是一個很好的學習工具，因為它會提供你可能經常犯但未注意到的語法錯誤的反饋，例如缺少閉合標籤和 HTML 中的多餘空格。

</div>

### 知識檢查

以下問題是對本課中的關鍵主題進行反思的機會。如果你無法回答問題，點擊它以複習材料，但請記住，你不需要記住或完全掌握這些知識。

- [DOCTYPE 宣告的目的是什么？](#the-doctype)
- [HTML 元素是什么？](#html-element)
- [Head 元素的目的是什么？](#head-element)
- [Body 元素的目的是什么？](#body-element)

### 其他資源

此部分包含與本課相關的有用鏈接。這不是必須的，所以可以作為補充材料考慮。

- 使用 [VSCode 的 Live Preview 擴展](https://marketplace.visualstudio.com/items?itemName=ms-vscode.live-server) 是打開 HTML 頁面的另一種選擇。這個擴展會打開你的 HTML 文件，並在你每次保存文件時自動刷新頁面。然而，我們建議你不要使用這個擴展，而是用傳統的方法手動打開和刷新頁面，這樣你可以習慣這個過程，而不會馬上依賴擴展。

- 如果你願意，你可以將 [lang 屬性](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/lang) 添加到整個網頁的個別元素。