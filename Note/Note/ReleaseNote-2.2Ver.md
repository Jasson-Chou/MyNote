專案名稱
[MAP Test Program Editor Solution]

版本號
版本: [版本號，例如 2.2.*] - Public
發布日期: [yyyy-MM-dd] - OS配合版本 1.9 Ver

新功能 (Features)
1.	增加Bin Table檔案建立
2.	增加Bin Table檔案編輯
3.	增加Bin Table (CSV、Excel)檔案的匯入及匯出
4.	增加Bin Table Template File的建立功能
5.	增加Bin Table的備份功能(對檔案選取SaveAs)
6.	增加Bin Table的備份功能(在Backup Project中選擇)
7.	增加Bin Table自動進版功能(當進入到這版本，會詢問使用者是否將FlowTable轉換成BinTable編輯方式，如需要則自動將使用者轉換並在SPJT選擇BinTable檔案，如不需要則選擇"否"將會繼續沿用FlowTable分Bin方式)
8.	當前Solution關閉Bin Table選項時，在Project Menu中會有Upgrade Bin Table Version的功能，供使用者升級使用。
9.	增加當Import Flow Table Excel File的版本限制。(如果與當前Solution設定不一致，會彈出錯誤訊息)
10.	增加當建立Template File完成之後，會詢問是否開啟Template File所在的資料夾位置。
11. 當檔案版本進版會顯示在Output中顯示進版訊息。
12.	增加檢查AWG檔案PinName之檢查，當在建置時。
13.	增加DPS Gang的檢查規則。
14. 增加Fatal Message顯示，若出現請聯繫AE。

改善 (Improvements)
1.	改善在Pin Group操作Pin的選擇方式，改善用戶體驗。
	在Apply之後會詢問是否刪除非定義的Pin，如果選"Yes"則自動幫使用者刪除，否("No")則保留使用者的編輯。
2.	顯示Pin Group未定義的所有Pin Name資訊顯示，當Project建置時。
3.	優化檔案版本更新時的程式邏輯。
4.	改善在SPJT編輯畫面過小，會部分區塊難以編輯的問題。
5.	Rename輸入無效字元時，會告知使用者非法的字元。
6.	在Signal Slot定義中，複製Cell內容會失敗
7.	禁止使用者重複建立新的Solution在相同位置。
8.	改善Timing Data建置時顯示錯誤的訊息完整性。
9.	優化Paste、Import、Replace Text(等一次性編輯大量Cell)時，所花費CPU時間占用過長問題。(目前測試使用效率提升約為98.57% 至 99.44% 之間，測試以1000個Pin和4個Site至32個Site來測試)
10.	改善部分使用者體驗操作。

Bug 修復 (Bug Fixes)
1.	修正Import SPJT Procedure未指定Solution版本到2.1的問題。
2.	修正AWG File在Load Project時產生的錯誤。
3.	修正掃描MAP OS版本資訊可能List不出來的問題。
4.	修正Signal Slot匯出Excel檔欄位計算錯誤的問題。
5.	修正Signal Slot編輯無法Copy文字的問題。
6.	修正部分Timing Data建置錯誤指示GUI的位置。
7.	修正當針對Solution進行Rename時，輸入相同名稱會導致*.msln消失的問題。
8.	修正建立Solution Project 和Solution Name時檢查是否合法機制。
9.	修正Pin和PinGroup頁面編輯Row或是Site數量時，不會觸發未儲存檔案符號(*)的顯示問題。
10.	修正Flow Table欄位Until Pass Count能夠設置小於0的情況。
11.	修正Limit Table欄位Up/Down Limit編輯完Lost Focus時數值不會顯示出來的問題。
12.	修正Editor關閉詢問時，點選x也會關閉的問題。
13.	修正Search/Replace Text定位功能。
14.	修正部分已知問題。

技術更新 (Technical Updates)
1.	更新Source File(signal, flow, ...)與UI Mapping關係(Field Mapper)，日後檔案/GUI欄位的增減更容易。
	(使用者在2.2版本之後的版本都能夠幾乎無痛降版，最低版本為2.2 Ver)

已知問題 (Known Issues)
某些稀有情況下，建置出來的Visual Studio有機率不成功。(手動打開剛剛所建立出來的Visual Studio，建置並查看失敗原因)
剛開啟Editor時，會觸發編輯過的狀態符號。(已解決，持續觀察中)

後續計劃 (Future Plans)
此版本會繼續維護Flow Tabel分Bin功能，預未來某一版2.X版本(含)之後全面改為BinTable分Bin。
預計在Version 2.X會更新Telerik元件以及將.net framework4.6.1升級至.net framework x.x.x。
增加Search/Replace Text針對單一檔案群組(例如:只Search or Replace Text當下Solution內的FlowTable Files)