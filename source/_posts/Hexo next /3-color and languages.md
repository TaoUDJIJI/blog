---
title: 【 架網站-3 】hexo的NexT主題：更換顏色篇（背景、頂部、側欄）、選擇網頁語言、修改語言文本內容
date: 2024-10-30 18:00:20
updated: 2025-1-28 17:00:00
tags:
  - 從零開始架設部落格
categories: 
  - 🌴 從零開始架設部落格-新手小白的學習筆記
---
> 選擇自己喜歡的顏色，佈置專屬自己的部落格

> 選擇網頁顯示的語言
<!-- more -->
## 更換背景顏色
+ 點選 <font color=#E86D2D>themes/next/source/css/_variables</font>，選擇自己主題的文件，例如 <font color=#E86D2D>Pisces.styl</font>，點入後搜尋 <font color=#E86D2D>$body-bg-color</font><font color=#909497> (快速搜索：mac 的話可以點command+F，windows 的話可以點control+F)</font> ，即可更改顏色，可上網搜尋「HTML顏色代碼」，查詢更多顏色的代碼，例如 「#CDE1F6」 就是淺藍色的代碼。
  {% codeblock %}
  $body-bg-color                = #CDE1F6;
 {% endcodeblock %}
<img src="https://i.imgur.com/rJ8K4gj.png"  width="90%" height="90%">

## 更換頂部顏色
+ 點選 <font color=#E86D2D>themes/next/source/css/_schemes_/Pisces</font> 的 <font color=#E86D2D>_header.styl </font>搜尋<font color=#E86D2D>「site-meta」</font>，於「site-meta」內新增一行 background 語法，以我為例我是選擇咖啡色。
{% codeblock %}
.site-meta {
  padding: 20px 0px;
  background: 顏色代碼
}
{% endcodeblock %}
<img src="https://i.imgur.com/2u41iOM.png"  width="90%" height="90%">

## 更換側欄顏色
+ 與上述更換頂部顏色的位置相同，於<font color=#E86D2D>_header.styl </font>內下方直接新增以下語法，以我為例我是選擇墨綠色。
{% codeblock %}
.header { 
  background: rgba(顏色代碼,1) none repeat scroll !important; 
}
{% endcodeblock %}
<img src="https://i.imgur.com/ZQZojiI.png"  width="90%" height="90%">

## 選擇網頁語言
+ **STEP1：**
點選 <font color=#E86D2D>themes/next/languages</font> ，會看見很多語言檔案，可以了解該主題有支持哪些語言，<font color=#E86D2D>zh-TW.yml</font> 是繁體中文，如果對於系統預設的文字不喜歡的話，可以直接在這邊改。
<img src="https://i.imgur.com/pVaUCDz.png"  width="90%" height="90%">

+ **STEP2：**
點選<font color=#E86D2D>「_config.yml」</font>，找到<font color=#E86D2D>「language」</font>，按照系統格式輸入想要的語言，像我選繁體中文的話，輸入 <font color=#E86D2D>zh-TW</font> 即可。
<img src="https://i.imgur.com/de8bMsZ.png"  width="90%" height="90%">
