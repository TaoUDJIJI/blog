---
title: 【 架網站-3 】hexo的NexT主題：更換顏色篇（背景、頂部、側欄）、選擇網頁語言、修改語言文本內容
date: 2024-10-30 18:00:20
updated: 2024-10-30 18:00:20
tags:
  - 從零開始架設部落格
categories: 
  - 🌴 從零開始架設部落格-新手小白的學習筆記
---
> 選擇自己喜歡的顏色，佈置專屬自己的部落格

> 選擇網頁顯示的語言
<!-- more -->
## 更換背景顏色
+ 點選 <font color=#E86D2D>themes/next/source/css/_variables</font>，選擇自己主題的文件，例如 <font color=#E86D2D>Pisces.styl</font>，點入後搜尋 <font color=#E86D2D>$body-bg-color</font><font color=#909497> (快速搜索：mac 的話可以點command+F，windows 的話可以點control+F)</font> ，即可更改顏色，可上網搜尋「HTML顏色代碼」，查詢更多顏色的代碼，例如 #CDE1F6 就是淺藍色的代碼。
  {% codeblock %}
  $body-bg-color                = #CDE1F6;
 {% endcodeblock %}

## 更換頂部顏色
+ 點選 <font color=#E86D2D>themes/next/source/css/_schemes_/Pisces</font> 的 <font color=#E86D2D>_header.styl </font>搜尋<font color=#E86D2D>「site-meta」</font>，於「site-meta」內新增一行 background 語法，變成：
{% codeblock %}
.site-meta {
  padding: 20px 0px;
  background: #225161
}
{% endcodeblock %}

## 更換側欄顏色
+ 與上述更換頂部顏色的位置相同，於<font color=#E86D2D>_header.styl </font>內下方直接新增以下語法：
{% codeblock %}
.header { 
  background: rgba(#9576b0,1) none repeat scroll !important; 
}
{% endcodeblock %}

## 選擇網頁語言
+ **STEP1：**
點選 <font color=#E86D2D>themes/next/languages</font> ，會看見很多語言檔案，可以了解該主題有支持哪些語言， <font color=#E86D2D>zh-TW.yml</font> 是繁體中文。

+ **STEP2：**
點選<font color=#E86D2D>「_config.yml」</font>，找到<font color=#E86D2D>「language」</font>，按照系統格式輸入想要的語言，像我選繁體中文的話，輸入 <font color=#E86D2D>zh-TW</font> 即可。

## 修改語言文本內容
+ 點選語言檔案，我是點選 <font color=#E86D2D>zh-TW.yml</font>，如果系統預設的文字不喜歡的話，可以在這邊改。例如針對「reward」這個詞，系統所的默認語言文本是「捐贈」，誒都...我覺得怪怪的，我把文本改成「抖內支持」。
