---
title: 【 架網站-9 】hexo的NexT主題：首頁及頁面配置篇（文章篇數顯示數量、先後順序、圓角化）
date: 2024-10-30 18:00:26
updated: 2024-10-30 18:00:26
tags:
  - 從零開始架設部落格
categories: 
  - 🌴 從零開始架設部落格-新手小白的學習筆記
---
>修改首頁顯示的文章篇數、決定網站顯示的先後順序、首頁配置的圓角化
<!-- more -->

## 修改首頁一頁顯示的文章篇數：
+ 於<font color=#E86D2D>「_config.yml 」</font>內修改，可以選擇首頁一次要顯示幾篇文章，也可以決定排序的方式。像我就是一頁顯示10篇文章，排序方式為日期。
``` 
index_generator:
  path: ''
  per_page: 10
  order_by: -date
``` 

## 決定網站顯示的先後順序：
+ 於<font color=#E86D2D>/source/_posts</font>目錄中，所放的檔案就是日後所發佈出去的文章，每篇文章點開後，最上方是基本資訊，其第一行、最後一行有用分隔線隔開，中間的內容包含標題、日期、標籤、分類。
像我排序方式是日期(date)，所設的時間越靠近現在，會顯示在首頁的前面，越以前的會顯示在後面，可以透過修改日期決定文章的排序。以我上一篇文章為例，這是我的基本資訊欄：
``` 
---
title: 【 架網站-8 】hexo的NexT主題：標籤篇（彩色標籤、文章底部標籤、標籤大小）
date: 2024-10-30 18:00:25 
updated: 2024-10-30 18:00:25 
tags:
  - 從零開始架設部落格
categories: 
  - 🌴 從零開始架設部落格-新手小白的學習筆記
---
``` 


## 首頁配置-圓角化：
+ STEP1：於<font color=#E86D2D>「_config.next.yml」</font>，搜尋<font color=#E86D2D>「custom_file_path」</font>，把「variable: source/_data/variables.styl」前面的＃刪除，以開啟該項功能。<font color=#4287B5>（（下方第10欄</font>

  ``` 
  custom_file_path:
    #head: source/_data/head.njk
    #header: source/_data/header.njk
    #sidebar: source/_data/sidebar.njk
    #postMeta: source/_data/post-meta.njk
    #postBodyStart: source/_data/post-body-start.njk
    #postBodyEnd: source/_data/post-body-end.njk
    #footer: source/_data/footer.njk
    #bodyEnd: source/_data/body-end.njk
    variable: source/_data/variables.styl
    #mixin: source/_data/mixins.styl
    #style: source/_data/styles.styl
  ``` 
+ STEP2：於<font color=#E86D2D>source/data</font>內新增<font color=#E86D2D>「variables.styl」</font>檔案，並新增以下語法：<font color=#4287B5>（可自行調整參數，決定圓角化程度）</font>

  ``` 
  // 圓角化
  $border-radius-inner     = 20px;
  $border-radius           = 20px;
  ``` 