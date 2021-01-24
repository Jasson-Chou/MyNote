[MapWidth] 使用者視窗寬度
[T0] Timing Resolution 由使用者定義
[Period] 由使用者定義
[PSPP] Point Size Per Period = Period / T0
[PPP] Pixel Per Period = Point Size Per Period * Time Unit Pixel
[Offset] Offset =  Scroll Value * PPP
[TP] Total Pixel = Period Size * PPP

找出使用者想看見畫面中的第一個Period Index

How to find [FPI] First Period Index
=> Offset < (FPI + 1) * PPP
=> FPI > Offset / PPP - 1 [整數除法]

找出使用者想看見畫面中的最後一個Period Index

How to find [LPI] Last Period Index
=> Offset + MapWidth >= LPI * PPP
=> LPI <= (Offset + MapWidth) / PPP [整數除法]


