# HW 4

> 「先寫 HTML 再來拆 component」和「先拆 component」的差別


## 先寫完 HTML 再來拆 component

> 其實我切 HTML 的經驗很少，好像只有幫朋友寫過一個公司形象網站和第一週的作業而已@@
> 工作後就直接用 Laravel blade 做專案，我還真的沒想過不拆 component 動態的東西要怎麼寫...

回想一下如果是沒什麼重複資料的網站（例如形象網站），我好像就會從上而下做，頂多拆 layout、header、footer、main。如果是差異不大的 RWD 網站會先做一版小版面，做完再來看大版面有什麼要調整。

> 參考：[第一次作業心得](https://github.com/jt6592/react-special/blob/master/blog/Special_1_front-end-basics.md)

## 先拆 component
起手式一樣是建 layout、header、footer、main。除了以版面切割，也會整理那些是重複出現的一組東西（講專業(?)一點就是 DRY），就是我的 component（元件）。我的 component 分兩種，靜態和動態（會傳資料進去）的，例如一個新聞網站，社群分享按鈕是靜態的，文章列表裡面的 ArticleItem 是動態的。

以我目前做的專案，我的 view 分 layout、components、page 三類，大概長這樣：

```
components
├ list_item
├－－ArticleItem
├ button
├－－SocialButtons
page
├ HomePage
├ CategoryPage
layout
├ base
├ header
├ footer
```

至於怎麼決定那些東西是一組的...其實就是依照人類的認知能力，將類似的東西依照形狀、性質...歸納、分類...無腦一點可以從資料來拆，一組資料就寫一個元件（講專業(?)一點就是關注點分離）。寫到這邊已經不知道要寫什麼了 orz

## 充字數
有關關注點分離的討論網路上有許多討論，其實在現代後端/全端的領域 MVC 已經是普遍的思維（或說程式設計規範？），除非你不用框架，不然是逃不過關注點分離的。但現在前端領域裡，簡單的畫面搭上一點動態呈現要使用框架似乎有點殺雞用牛刀，所以這種摻在一起做撒尿牛丸的前端程式碼也還滿常見的。就像被唾棄的 php 義大利麵，在搭上 Laravel 之後變得簡潔、優雅。既然使用了前端框架就是想要有被規範的好處，我想在未來 JavaScript 應該也是如此ㄅ

## 參考
* [關於HTML與JS混雜這件事](https://www.ithome.com.tw/voice/133525)
* React 官網 [怎麼拆 component](https://zh-hant.reactjs.org/docs/thinking-in-react.html)