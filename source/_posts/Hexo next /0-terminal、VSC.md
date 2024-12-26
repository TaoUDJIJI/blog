---
title: 【 架網站-0 】起手式：「終端機」、「Visual Studio Code」
date: 2024-10-30 18:00:17
updated: 2024-10-30 18:00:17
tags:
  - 從零開始架設部落格
categories: 
  - 🌴 從零開始架設部落格-新手小白的學習筆記
---
>終端機 (terminal)：適用於進階使用者和開發者，透過輸入指令與電腦互動，可以用來執行簡單到高度複雜的作業。
>Visual Studio Code：為Markdown語法的程式碼編輯器，可以加快Markdown的編寫速度。
<!-- more -->
## <font color=#E86D2D>終端機：</font>
### 查看有無下載好：「 -v」
+ 安裝完後，可輸入「<font color=#4287B5>安裝的名稱 -v」</font> ，像我有安裝的是「node」、「git」，如果有安裝成功的話下方會出現版本號碼或跑出東西。
### 啟動Hexo伺服器：輸入「hexo s」
>我每天都會關機電腦，當天第一次開啟終端機時，都需要「移動當前位置」
+ **<font color=#4287B5>以我為例，移動軌跡：要從「～」移動到「Desktop」的「blogger_UD2」</font><font color=#909497>（這是我hexo所在的資料夾）</font>** 

  **STEP1：從「～」移動到「Desktop」**
  「～」代表當前位置跑到最上層的資料夾<font color=#909497>(另補充查看當前位置的指令是「pwd」)</font>，在<font color=#4287B5>「主機名稱 ～ %」</font>後面輸入「cd」，接著連續按「tab鍵」兩下<font color=#909497>（cd是移動的指令，tab點兩下是快速查找當層位置有哪些資料夾，另補充「cd ..」是退回到上一層）</font>，可找到「Desktop」，把它複製起來貼在「cd」後面即可，當前位置就變成<font color=#4287B5>「主機名稱 Desktop %」</font>。

  **Step2：從「Desktop」移動到「blogger_UD2」**
  在<font color=#4287B5>「主機名稱 Desktop %」</font>後面輸入「cd」，接著連續按「tab鍵」兩下，可找到桌面上的「blogger_UD2」的資料夾，把它複製起來貼在「cd」後面即可，當前位置就變成<font color=#4287B5>「主機名稱 blogger_UD2 %」</font>。
+ **<font color=#4287B5>當「當前位置」已在hexo所在的資料夾後，輸入「hexo s」</font>** 
「http://localhost:4000/blog/」
會出現上方這一串網址，這是只有自己看得見的網頁，途中可以透過寫程式更改網頁的樣式、內容，逐漸建構屬於自己的網頁。

### 停止Hexo伺服器：輸入Ctrl+C 
+ 於終端機頁面直接按「Ctrl+C」即可關閉「Hexo伺服器」，長時間不用就可以先關閉省電，關閉後隨時想用時再直接輸入「hexo s」即可，不是每次關閉都要移動當前位置，只有當天第一次使用才需要移動。

### 清理Hexo伺服器緩存：hexo clean
+ 如果有更改網頁的樣式、內容但網頁卻沒有隨之更新時，先按「Ctrl+C」關閉「Hexo伺服器」，接著於終端機輸入「hexo clean」即可清除緩存，清除完緩存後輸入「hexo s」重啟「Hexo伺服器」，內容即會更新完成。

## <font color=#E86D2D>Visual Studio Code</font>
+ 是一款由微軟開發且跨平台的「免費原始碼編輯器」，我都使用這個編輯網頁，使用上很方便，直接把hexo所在的資料夾拖移進來即可，以我為例，直接把「blogger_UD2」拖入，即可編輯「blogger_UD2」的內容。
+ 常用快捷鍵：
「Mac電腦」按鍵跟「Windows電腦」按鍵不一樣，我有找到[ APPLE官方對照表](https://support.apple.com/zh-tw/guide/mac-help/cpmh0038/mac)，可以參考看看，**「Windows電腦」的Control鍵等同「Mac電腦」的Command鍵**。
   + 全選：	Command鍵 / Control鍵 ＋A
   + 儲存：	Command鍵 / Control鍵 ＋S
   + 剪下：	Command鍵 / Control鍵 ＋X
   + 尋找：	Command鍵 / Control鍵 ＋F
   + 回到上一步：	Command鍵 / Control鍵 ＋Z
