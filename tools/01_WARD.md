
# WRDS
website direct link:
https://wrds-www.wharton.upenn.edu/login/

Wharton Research Data Services（WRDS）是由賓州大學華頓商學院所建立的整合型資料庫平台，其功能主要為讓資料庫整合介面讓檢索更便利，驗證資料正確性。結合多個財經商學資料庫內容涵蓋全世界各主要國家股票、債券、期貨之交易資料，及財務報表、盈餘預測、創投、初次上市櫃等相關資料庫，完整蒐集全世界上市上櫃公司資訊與股價變動現象。(资料来源：https://management.ntu.edu.tw/CSIC/DB/WRDS)

# How to have a WRDS account?
申請步驟：
Step 1: 到WRDS網站:https://wrds-www.wharton.upenn.edu/login/ 註冊新帳號，並到信箱點擊確認信；
Step 2: 到線上表單填報申請審核(https://forms.gle/hnP94tJ4fFSZC5o39)；
Step 3: 通過審核，系統寄發審核通過信件，按指示操作。若有相關問題，請洽林小姐(yulin@lib.nycu.edu.tw)。



# How to download data from WRDS?
## 1.登录WRDS账号
![](https://i.imgur.com/k7AA9WO.png)
## 2.點選 Get Data，並選則下方的 All Data 
![](https://i.imgur.com/11U2Bwk.png)
## 3.這裡面是各個資料庫的名稱。
### 3.1 其中藍色的部分是學校有購買的，灰色部分是學校沒有購買的。
### 3.2 舉例來講，
**大股東（Blockholders）**：該數據集包含1,913家公司的大股東的標準化數據。
**CRSP ( Center for Research in Security Prices )** CRSP保留了最全面的紐約證券交易所(NYSE)、美國證券交易所(AMEX)和納斯達克(NASDAQ)股票市場證券和衍生商品之數據。CRSP研究中心位於芝加哥大學商學院的研究機構，由其維護由1925年12月至今之歷史數據。
**Compustat ( Compustat North America )**
提供北美超過7500家上市公司300多個年度和100個季度的損益表、資產負債表、現金流量表和補充數據項目。絕大部分之公司均可取得最近20個年度及48個季度之數據。
**OptionMetrics**
美國股票和指數期權市場的歷史價格和隱含波動率數據的綜合來源。數據庫包含期權及其相關基礎工具的歷史價格，正確計算隱含波動率和期權敏感度。數據可從1996年至今。
(资料来源：https://management.ntu.edu.tw/CSIC/DB/WRDS)

### 3.3 並且，現在右邊有新增Concept，有幫你歸類，比如說，你點擊banks就會出現bank相關的所有資料庫。
![](https://i.imgur.com/tc2UZag.png)

## 4 Take CRSP as an Example
### 4.1 點擊CRSP進入 
![](https://i.imgur.com/jnoqIkf.png)
### 4.2 如果要下股價資料，點擊stock/security Files進入
![](https://i.imgur.com/4M1xIhE.png)
### 4.3 如果要下日资料，點擊Daily stock file進入

#### 1.在step1:choose your date range中可以選擇你需要的資料期間。(在這個例子裡因為日資料非常大，所以如果資料期間很長，資料量也會非常大) 
 
##### 2.在step2：Apply your company codes 一般我都會使用search the entire database。但是如果你已經有確定的公司名單，那可以用公司的TICKER/PERMNO/PERMCO/CUSIP/NCUSIP/HSICCD/SICCD來直接搜尋。從Browse 中上傳code list，來進行搜尋。
![](https://i.imgur.com/ph0v1Lc.png)

#### 3.step3： choose query variables 這是讓你選擇你需要資料庫裡的哪些變數，一般我點選select all
![](https://i.imgur.com/saJ6N42.png)

#### 4.Step4：select query output 這一步在選擇你需要的輸出格式，可以根據你的需求調整，以下是我常選的格式。最后点击Submit Form
![](https://i.imgur.com/LnIuPvD.png)

#### 5. 然後會出現如下的頁面，表示你要下載的資料正在run，根据你的資料大小，要等的時間可能會有差別
![](https://i.imgur.com/FDeTWab.png)

#### 6. 下載好之後，它會顯示 success，然後你可以點擊output files查看你的資料
![](https://i.imgur.com/CWI4f1p.png)

###  7.补充
以上的過程只使用了Query Form，那如果要瞭解跟資料相關的別的內容，可以在variable Descriptions、Manuals and Overviews、knowledge Base、Data Dictionary中尋找。例如， Variable Descriptions 中有變數的基本定義，那有些資料庫會在Data Dictionary中有更詳細的定義。
 當然，如果你有一些問題，比如有些變數應該怎麼計算之類，你也可以嘗試在搜尋框中搜尋。

![](https://i.imgur.com/ZhqJy9S.png)

written by Ning Tang
:::success
1. Quick start to [HackMD](https://hackmd.io/8nPFj8X7Rc2UhkhfjYAbkw)
2. Write-up for downloading data in [TEJ](https://hackmd.io/LfakJmiPQCauy48zAx71xw)
3. See you around 2021/11/12. 
:::







