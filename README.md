# PyConTW2018Talk
土炮一個 Line 股票機器人

投影片連結：

* [https://bit.ly/2kGkOxq (上)](https://bit.ly/2kGkOxq)
* [https://bit.ly/2J161fo (下)](https://bit.ly/2J161fo)


機器人 QR Code:

![土炮股票機器人](https://github.com/victorgau/PyConTW2018Talk/blob/master/images/C0BD_CPlDR.png)

稍微說明一下：

* 即時股價是直接抓證交所的資料，查詢的次數太"頻繁"的話，證交所會把之後的 request 擋掉。所謂的"頻繁"，其實也沒有那麼頻繁，很容易的就會被擋掉了。
* 歷史股價的部份是從 Yahoo Finance 直接抓，多張股票的時候會等比較久。
* 圖片的部份因為需要先上傳 imgur，再把連結傳回來，所以花的時間會比較久。
* 回測的部分，因為要下載多張股票的歷史資料，回測結果又要上傳 imgur，所以花的時間會比較久。
* 觀察股的數量目前限制為 5 檔股票。

指令大概是這些：

    #股票代號 ==> 查詢即時股價
    $股票代號 ==> 投資建議
    /股票代號 ==> 繪製 K 線圖
    !list ==> 列出觀察股
    !add 股票代號 ==> 加入觀察股
    !del 股票代號 ==> 刪除觀察股
    !backtest ==> 回測觀察股清單中的所有股票
    !news n ==> 列出 n 則鉅亨股市新聞 (n < 30)

程式是在演講前才寫好的，所以沒做甚麼 exception handling，如果它沒回應的，歡迎傳訊讓我知道一下，可能是被試到掛掉了。