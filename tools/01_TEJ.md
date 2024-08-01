
Originally written by Mr. 李國誠 (Summer, 2021). Reviewed by Huei-Wen Teng


# TEJ

1. [第一次TEJ Pro 就上手](http://www.tej.com.tw/TEJPLUS/%E3%80%90TEJ%E3%80%91%E7%AC%AC%E4%B8%80%E6%AC%A1%E7%94%A8TEJPro%E5%B0%B1%E4%B8%8A%E6%89%8B.pdf)
2. [TEJ 資料庫項目一覽表](http://www.tej.com.tw/webtej/doc/list.htm)
3. [資料介接 API](https://api.tej.com.tw/index.html)
4. [鉅亨網](https://www.cnyes.com/)
5. 國誠協助TEJ抓mutual fund. 
6. http://tej.lib.nctu.edu.tw/download/


### Demo: Download daily fund prices in TEJ


下載共同基金資料。

| Index |csv | 基金碼 | 簡稱 | Start date | End date | 幣別 | 
| -----| -------- | -------- |-------- | -------- |-------- | ----| 
|1 | 01010T     | 2    | 第一金福元     |20000104| 20140624| NTD|
| 2| 01010T | 3 | 匯豐成長| 20000104| 20111125|NTD|
| 3| 01010T | 6 | 荷銀鴻福 | 2000104| 20001204| NTD|




1. 打開TEJ。本安裝程式限 交通大學 IP 範圍內使用，進入帳號 (USER ID)：NCTU ，密碼(PASSWORD)： TEJ
2. 點選左側TEJ FUND DB 兩下
3. 接著點選基金淨值兩下! 

[](https://i.imgur.com/9uk8s0n.png)

6. 點選畫面左上方的特殊轉檔。特殊轉檔的好處在於它可以把資料匯出成txt，csv等格式。另外，在匯出資料時也沒有筆數限制。但因為我們這次匯出的資料量非常大，我還是選擇分批將資料匯出。
![](https://i.imgur.com/eXClQtA.png)

5. 這邊以一次取15個基金過去20年的資料為例:
    - 將這15個基金選取後按下圖中的單箭頭，這些基金就會跳到右邊的方框
    ![](https://i.imgur.com/pAqMr5S.png)

    - 接著選取想要的資訊。這邊選的是幣別，淨值，市價。同樣按下單箭頭讓資料跳到右邊的方框。
    ![](https://i.imgur.com/6sAHf5i.png)
    - 設定時間:勾選右上方的"自選日期"後點選日期選單。接著將日期區間設為2000/01/01-2021/07/31，查詢。把降冪取消，最後點選圖中的雙箭頭(全部選取)，按下確認。
        ![](https://i.imgur.com/7KY9KGV.png)
    - 將分隔符號從tab改成逗號。
        ![](https://i.imgur.com/OXCJW1s.png)
    - 顯示空值字串改成N.A. ，取消勾選"依日期排序"
    ![](https://i.imgur.com/Yz6PvZK.png)

    - 點選存檔位置，在桌面新增一個檔案，檔案類型選擇csv，點選存檔。
    ![](https://i.imgur.com/dPmMDZ4.png)
    - 按下開始轉檔，成功轉檔會跳出下面的畫面![](https://i.imgur.com/N4g9e5R.png)




:rose: 陽交大已購置TEJ使用權限，若有問題，歡迎聯繫以下負責人員(Aug, 2021)。
![](https://i.imgur.com/FpvCQlW.jpg =188x), ![](https://i.imgur.com/Qc2GoBl.jpg =188x)



