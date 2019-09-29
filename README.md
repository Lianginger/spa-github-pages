# Single Page Apps for GitHub Pages

[Demo site](https://lianginger.github.io/spa-github-pages/)

在 GitHub Pages 上部屬 Single Page Apps，會遇到分頁重新整理跳錯的問題，利用[客製化的 404.html](https://github.com/Lianginger/spa-github-pages/blob/master/404.html) 進行頁面跳轉，例如將：  
`https://lianginger.github.io/spa-github-pages/list` 頁面重導向  
`https://lianginger.github.io/spa-github-pages/?list`

再由 [index.html 程式](https://github.com/Lianginger/spa-github-pages/blob/65b6f46938e715db22111f616d31552acb7ba7a0/index.html#L49) 取得 Query String( ?list )，做頁面切換，最後用 `window.history.pushState(null, null, list)` 操控瀏覽器歷史紀錄，讓網址列顯示  
`https://lianginger.github.io/spa-github-pages/list`

![Demo GIF](https://github.com/Lianginger/spa-github-pages/blob/master/demo.gif)

參考資料 [淺談新手在學習 SPA 時的常見問題：以 Router 為例](https://blog.huli.tw/2019/09/18/spa-common-problem-about-router/)、[aszx87410/spa-problem-demo](https://github.com/aszx87410/spa-problem-demo)、[afrex/spa-github-pages](https://github.com/rafrex/spa-github-pages)
