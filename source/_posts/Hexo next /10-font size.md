---
title: 【 架網站-10 】hexo的NexT主題：調整字體大小篇（font-size）
date: 2024-10-30 18:00:27
updated: 2024-10-30 18:00:27
tags:
  - 從零開始架設部落格
categories: 
  - 🌴 從零開始架設部落格-新手小白的學習筆記
---
>font-size-base、font-size-smallest、font-size-smaller、font-size-small、font-size-medium、font-size-large、font-size-larger、font-size-largest
<!-- more -->

## 調整字體大小：
+ 位置：<font color=#E86D2D> themes/next/source/css_variables/base.styl </font>
+ 下面參數我都一個個調，去找網頁有哪邊不一樣，但「font-size-larger」沒特別看出來有什麼變化，下方參數是我修改後的，大家各憑喜好可以自行調整字體參數大小。
 ``` 
// Font size
$font-size-base           = (hexo-config('font.enable') and hexo-config('font.global.size') is a 'unit') ? unit(hexo-config('font.global.size'), em) : 0.95em;
$font-size-smallest       = 0.90em;
$font-size-smaller        = 1.00em;
$font-size-small          = 0.875em;
$font-size-medium         = 1.1em;
$font-size-large          = 1.025em;
$font-size-larger         = 1.0em;
$font-size-largest        = 1.1em;
 ``` 
### font-size-base：
+ 我把網頁發佈到 Github 上面的時候發現網頁整體比例太大，就調成0.95em。
### font-size-smallest ：
+ 每篇文章上方資訊（如：發表時間2024-10-30、分類於🌴 從零開始架設部落格-新手小白的學習筆記）
+ 首頁側邊欄位「歸檔」的內頁，每篇文章前面的日期 <font color=#909497>（（不含文字</font>
### font-size-smaller ：
+ 側欄的導引（首頁、關於、標籤、分類、歸檔、搜尋）
+ 作者欄位的文字（說明欄、文章、分類、標籤） <font color=#909497>（（不含數字</font>
### font-size-small ：
+ 首頁的頁尾資訊（2024 TaoUD、訪客人數與觀看次數、由 Hexo & NexT.Gemini 驅動）
+ 文章內頁點開後，側欄的目錄
+ 文章內頁點開後，頁尾的「前、後篇文章」欄位
### font-size-medium ：
+ 作者欄位的數字（「75」篇文章、「6」分類、「12」標籤） <font color=#909497>（（不含文字</font>
### font-size-large：
+ 文章的內文
+ 首頁側邊欄位「分類」的內頁
### font-size-larger：
+ 沒有看出什麼變化
### font-size-largest：
+ 每篇文章的標題、側欄導引（首頁、關於、標籤、分類、歸檔）點開內頁後的標題

## 調整網頁整體大小：
會有整體比例一起縮小的感覺，在我實驗下，與「font-size-base」的功能相似，所以後來我只有改「font-size-base」參數，這邊就沒有動。
+ 修改前語法：
 ``` 
font:
  enable: false

  # Uri of fonts host, e.g. https://fonts.googleapis.com (Default).
  host:

  # Font options:
  # `external: true` will load this font family from `host` above.
  # `family: Times New Roman`. Without any quotes.
  # `size: x.x`. Use `em` as unit. Default: 1 (16px)

  # Global font settings used for all elements inside <body>.
  global:
    external: true
    family: Lato
    size:
 ``` 
 + 修改後語法：<font color=#4287B5>（（ 「enable」改成 true、「size」後填上數字</font> 
 ``` 
 font:
  enable: true

  # Uri of fonts host, e.g. https://fonts.googleapis.com (Default).
  host:

  # Font options:
  # `external: true` will load this font family from `host` above.
  # `family: Times New Roman`. Without any quotes.
  # `size: x.x`. Use `em` as unit. Default: 1 (16px)

  # Global font settings used for all elements inside <body>.
  global:
    external: true
    family: Lato
    size: 0.95
  ``` 