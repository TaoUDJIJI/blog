---
title: 【架網站】網頁背後的秘密-markdown語法
date: 2024-02-22 18:00:18
updated: 2024-02-22 18:00:18
tags: 從零開始架設部落格
categories: 
  - 🌴 從零開始架設部落格-新手小白的學習筆記
---
># markdown筆記
>練習篇
利用hackMD做筆記
<!-- more -->
## <font color=#E86D2D>文字篇：</font>
### <font color=#E86D2D>一、標題：＃</font>
<font color=#FF5656>＃要空一格在打字。</font><font color=#2E86C1>＃x6</font> 的大小跟＃x5一樣，只是<font color=#2E86C1>會變成灰色</font>  
＃x7無效
# 我是標題 
## 我是標題
### 我是標題
#### 我是標題 （大小跟內文差不多，只是變粗）
##### 我是標題
###### 我是標題 (變成灰體字了)

<!-- more -->
<https://www.youtube.com>
[youtube](https://www.youtube.com)

[誒你這週要幹嘛](https://www.youtube.com/watch?v=vIpvoRqLupo&ab_channel=%E6%AC%B8%E4%BD%A0%E9%80%99%E9%80%B1%E8%A6%81%E5%B9%B9%E5%98%9B)

### <font color=#E86D2D>二、字體：</font>
+ 我是內文
+ ：
> 文字的前後加上兩個波浪號~~
，打上後程式欄自動會出現刪除號，不用理它
+ <font> <u>我是底線</u> </font> 
> 文字前後只加上<u.>(故意在u後面打了一個小點點
> 不然顯示不出來)
 實驗結果：發現當前頁面整篇都會有底線，
 解決方法：使用<font color=#FF5656>閉鎖代碼</font>：<font color=#FF5656><font.></font> 指令 <font color=#FF5656></font.></font>
 因為文字兩側是<u.>，為了閉鎖代碼，在<u.>外側以對稱的<font.> 字包圍，文字後者的代碼要加上斜線，變成</u.></font.>，這樣就能只鎖定特定區域發生效果。
 
+ *我是斜體*
+ ***我是粗斜體***
+ **我是粗體** 
<font color=#FF5656>（Q:下方1. 2.的格式好亂，
    A:找到原因了！點點後面要加上空格再打文字）</font>
 1. ＃x4的大小跟直接打字一樣，差別在<font color=#2E86C1>加＃會變粗體</font>
#### 實驗結果：1.＃x4與前、後行的行高都會隔一行寬
 無法直接當內文使用

2. \*x2文字\*x2（全形、半形有別別打錯，分別為＊、*）
**粗體、大小等同於＃x4**，但在**段落上**有不同，
此語法可以直接當內文使用，**不會多空一行**
 
### <font color=#E86D2D>三、顏色：</font>
+ [<font color=#909497>顏色代碼-網址請點入內</font> ](https://htmlcolorcodes.com/zh/yanse-xuanze-qi/)
語法：<font. color=<font color=#909497>顏色代碼</font>>打上想要被著色的文字</font.> 
<font color=#6b8e23>軍綠色is me</font> 
<font color=#2E86C1>中藍色is me</font> 
<font color=#2698C2>藍綠色is me</font>
<font color=#09B5F8>淺藍色is me</font>
<font color=#AA68C5>淡紫色is me</font> 
<font color=#d2691e>紅咖色is me</font> 
<font color=#cd853f>淺咖色is me</font> 
<font color=#E86D2D>髒橘色is me</font>
<font color=#F85518>橘紅色is me</font>
<font color=#FF5656>紅色is me</font>
<font color=#F18C24>橘色is me</font> 
<font color=#ff69b4>粉紅色is me</font> 
<font color=#000000>黑色is me</font> 
<font color=#6B6E71>深灰色is me</font> 
<font color=#909497>淺灰色is me</font> 
<font color=#ffffff>白色is me</font> 
### <font color=#E86D2D>四、內文：</font>
#### <font color=#E86D2D>1.標記文字：</font>
<font color=#2E86C1>語法：文字前後加上 == </font> 
同一個語法在Hexo server不成功，但在hackMD有成功
==waku waku==
#### <font color=#E86D2D>2.表格：</font>
同個語法在Hexo server沒有表格中間的線，在hackMD則有
>第一列是表格的標題列，
第二列固定要是以 --- 做區隔，加欄位都是使用 | 來添加。
注意表格的每欄寬度會自動分配，
所以可以忽略一切的空格(也就是每列的 | 沒有對齊也沒關係，
加多少空格也不會影響每欄的寬度)。
而每欄可以決定要如何對齊，對齊方式取決於第二列的 ---，
:--- 靠左對齊。
---: 靠右對齊。
:---: 置中對齊。
+ 置中

|天氣  | 適合活動 |
| --- | --- |
|晴    | 逛展覽瓜瓜瓜瓜 |
|涼爽 |騎腳踏車  |
|毛毛雨    | 在家看電視 |
+ 靠左

|天氣  | 適合活動 |
| :--- | :--- |
|晴    | 逛展覽瓜瓜瓜 |
|涼爽 |騎腳踏車  |
|毛毛雨    | 在家看電視 |
 
![花](https://www.flowerdj.com/x/images/product/AE/AE282_x.webp)