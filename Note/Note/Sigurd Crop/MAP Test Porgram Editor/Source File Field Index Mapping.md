Outline
Mapper 更動原因/更動概念
Site處理方式
命名規則



Mapper 更動原因/更動概念

以MAP Editor 2.0版本發現，當使用者所要的多增加功能，會導致編輯欄位要新增或是刪除時，Source File變動會很大(Index更動容易出錯，且退版本使用者如果沒有備分的話，則會花費較多時間復原)。

所以後面加入Source File Mapping概念，圖如下:
當新增的欄位要插入至GUI中間會導致檔案要更動。(因GUI上欄位顯示是依照檔案中C'1'、C'2'上面的數值所定位的，所以當降版本會倒置相關欄位皆會位移)
![[Pasted image 20241121121244.png]]
Source File:
<R0 C6="ON" C1="ON" C2="ON" C4="TestField1" />
<R1 C6="ON" C1="ON" C2="ON" />
<R2  C4="TestField2" />
<R5  C4="TestField2" />

![[Pasted image 20241121135754.png]]


為了解決上述問題，後面想出了 [Source File Field Index Mapping] 方式，使得後續要增減欄位不會有使用者在使用上，承受更大的風險來解決資料不見或是表格位移的情況發生。
解決方式:

增加File Field Index Mapping層
![[Pasted image 20241121135811.png]]

解決了退版檔案無法使用，和進版修改過於麻煩的問題。

為什麼不用欄位名稱定義至檔案內?
Example:
Source File:
< R0 
AutoPowerDown="ON" ContinuOnACFail="ON" StopOnFail="ON" myTestField1="TestField1" />

原因不推薦: 除非能夠確保欄位未來不做更改，不然退版時也會面臨資料遺失的問題。


Site處理方式

目前2.2版本定義

Site數量最大為1024個(0 ~ 1023 Sites)


命名規則

GuiFieldIndex => SrcFieldIndex
SrcFieldIndex => GuiFieldIndex

Gui和Src是能夠互相轉換的