# React:1 與前端相關的為什麼

這一堂課程講的是前端的一些基礎觀念，每一個提到的東西其實都可以長篇大論。
不想寫一篇很淺的前端大雜談，但想寫深的又沒那個知識深度與時間，因此這次採用問答的方式記錄談到的東西。
另外就是我自己很喜歡十萬個為什麼、圖文小百科之類的書。

## 前端雜談


什麼是網頁（webpage）、瀏覽器（browser）、為什麼看得到網頁？
瀏覽器是一隻程式，瀏覽器實作 W3C 規範（HTML/CSS/JavaScript），能解析（畫）出前端看到的畫面，網頁就是「看到的畫面」。

-----

HTML 是什麼？
HTML/CSS/Markdown 都是靜態標籤檔案，只要有對應的軟體就能讀，就像 .doc 可以用 MicroSoftWord 讀取

-----

為什麼上網可以看到網頁、瀏覽器怎麼透過跟伺服器拿 HTML？
瀏覽器會透過 protocol （常見的如 HTTP） 去跟伺服器要檔案。
瀏覽器當然也可以讀本地的檔案，這時會用 protocol file 讀取 .html 檔

-----

什麼是靜態網頁、動態網頁？
靜態網頁 -> 把 HTML 靜態檔案放在伺服器上
動態網頁 -> HTML 是用程式（NodeJS、PHP、Python...）產生出來的

-----

HTML 是什麼？
HTML/CSS/Markdown 都是靜態標籤檔案，只要有對應的軟體就能讀，就像 .doc 可以用 MicroSoftWord 讀取

-----

為什麼上網可以看到網頁、瀏覽器怎麼透過跟伺服器拿 HTML？
瀏覽器會透過 protocol （常見的如 HTTP） 去跟伺服器要檔案。
瀏覽器當然也可以讀本地的檔案，這時會用 protocol file 讀取 .html 檔

-----

什麼是靜態網頁、動態網頁？
靜態網頁 -> 把 HTML 靜態檔案放在伺服器上
動態網頁 -> HTML 是用程式（NodeJS、PHP、Python...）產生出來的

-----

為什麼要命名？我不能 div 到底嗎？
你當然可以，但是...
* 命名在 React 是很重要的，一個專案隨便都有一百個 Component
* 你可以更快的完成一個案子
* 以及 **SEO** （請愛用語意化標籤QQ）

-----

寫到這邊發現有些東西好像不太能夠用問答呈現
只好先邏輯分裂，以下又變成心得文 @@

-----

## 筆記

### 有關切版 HTML 結構...

#### 一、`<header></header>` 導覽列
```
NavBar/NavItem
```

> 延伸討論：nav 到底是 NavBar 還是 NavItem

#### 二、`<main></main>` 區塊內
```
        外壁 
        容器 
        內壁 
        row
        col
        item
```
1. 外壁
通常使用 HTML section 標籤。
如果是滿版背景我會在這一層下 bg-color

2. 容器 
通常框架或 CSS 命名使用 conainer，通常會在這一層控制 max-width。
Tailwind 寫法是 .container .mx-auto

3. 內壁 
在這一層控與內壁的距離。
我會在這一層做內/外距(margin/padding)與排版(flex/grid)

4. row & col
網頁是由上往下捲動，現在主流 RWD 是流動排版，也就是一欄滿了東西要往下掉。
row 用來控制橫向的區塊、col 則是直向的布局。
row 與 col 其實也是排版的容器，不應該有內/外距，應該就單一職責的做流動排版，避免莫名的被擠爆。

5. item
item 在 bootstrap 叫作 card，但有些東西明明不像 card XD

### 有關切版 CSS 結構...

#### BEM CSS

### 有關 SEO

#### 1.加速你的網站 -> 減少 first rendering 時間

* minify -> 刪除空格
* uglify -> rename variable
* bundle -> 減少 request、blocking, ajax 堵塞
    通常會依照功能分 bundle，一支超巨大bundle .js 也不好

前端的打包工具 -> webpack, gulp

-----

2.結構化資料

* JSON-LD
* 語意化標籤


