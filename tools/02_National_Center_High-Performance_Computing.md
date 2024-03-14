---
title: 20230711 國網中心
tags: finalytics
---

# 國網中心

- Editor by Ian Lee on 20230711
- Reviewed by Teng


## 以個人為單位註冊帳號
1. 先至國網中心官網(https://www.nchc.org.tw/)，下滑至計算資源服務網，左側點選前往申請。![](https://i.imgur.com/iJJ9uoF.png)
2. 右上角點選註冊，並填寫完註冊資料，完成註冊流程。主機帳號可自行設定，方便記憶就好，後續也可查詢。![](https://i.imgur.com/rICrBRg.jpg)
3. 發送"會員帳號(即註冊的email)"給鄧老師(venteng@gmail.com)，鄧老師會將每人的帳號登錄至計畫內，並分派資源額度
4. 使用[TWCC服務](https://www.twcc.ai/)執行python jupyter，請參考[開發型容器的使用說明](https://man.twcc.ai/@twccdocs/doc-ccs-main-zh/https%3A%2F%2Fman.twcc.ai%2F%40twccdocs%2Fguide-ccs-create-zh)
    * 除非同學確定要跑的運算量非常大，否則在建立容器的時候，建議先選取最基本的配備，以節省被分配到的子錢包額度
    * <font color="#f00">建立容器後，即刻開始依照時數收費，請不需要使用的時候，**刪除容器**。可以先建立複本，下次要建立容器比較快。</font>
5. 進入jupyter介面後，若無法上傳檔案(下圖upload處)，請參考以下步驟。若上傳成功，請直接跳至第9點
![](https://i.imgur.com/BZorUk7.png)


6. 下載[WinSCP](https://winscp.net/eng/download.php)。開啟後，將遠端登入資訊依序填入。資訊請至TWCC內的「開發行容器詳細資料」找尋。依照下二圖範例填入。
![](https://i.imgur.com/Y015GpU.png)
![](https://i.imgur.com/3yGW6NZ.png)
7. 填入主機密碼
![](https://i.imgur.com/oge6DDs.png)

8. 挑選/work或/home上傳資料，下圖以/work為例，直接將檔案從左邊的個人電腦目錄拖移至右側的遠端/work/(主機帳號)目錄即可。
![](https://i.imgur.com/n4zvCU5.png)

9. 上傳成功後，回至jupyter重新整理，並讀取資料進行分析。以上傳至主機帳號為i309554038、目錄為work為例來讀取資料。
![](https://i.imgur.com/VSEN9Lz.png)


## 其他問題
若有上傳資料相關問題，請與助教聯絡，或參考[常見問題](https://man.twcc.ai/@twccdocs/doc-ccs-main-zh/%2F%40twccdocs%2Fccs-overview-zh)
## 障礙排除

請洽國家高速網路與計算中心客服小組:

●免付費客服專線 0809-091-365
●服務時間：9:00~17:00(週一至週五)，國定、例假日除外
●電子郵件技術支援
帳號申請服務電郵：iservice@twcc.ai
技術支援服務電郵：isupport@twcc.ai





## 其他問題

1. [錢包管理說明1](https://iservice.nchc.org.tw/nchc_service/nchc_service_qa.php?target=16)
2. [錢包管理說明2](https://iservice.nchc.org.tw/module_page.php?module=nchc_service#nchc_service/nchc_service.php?action=prj_view_wallet&uuid=a487afa6-a769-4d32-b232-222b83204537)
