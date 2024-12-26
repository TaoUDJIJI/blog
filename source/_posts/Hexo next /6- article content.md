---
title: 【 架網站-6 】hexo的NexT主題：文章內文篇（超連結顏色、閱讀全文、文章更新、目錄、程式區塊）
date: 2024-10-30 18:00:23
updated: 2024-10-30 18:00:23
tags:
  - 從零開始架設部落格
categories: 
  - 🌴 從零開始架設部落格-新手小白的學習筆記
---
>包含撰寫文章、連結顏色更改、新增閱讀全文按鈕、文章顯示更新時間、側欄-目錄、程式區塊
<!-- more -->

## 撰寫文章：
+ <font color=#E86D2D>/source/_posts</font>目錄中，所放的檔案就是日後所發佈出去的文章，想新增文章的話可以在「終端機」輸入「hexo new page」指令，也可以直接在當初下載HEXO的資料夾內新增文章。每篇文章點開後，最上方是基本資訊，其第一行、最後一行有用分隔線隔開，中間的內容包含標題、日期、標籤、分類（<font color=#909497>當然，這一切取決於自己的需求，都可以做更改刪除</font>），以我第8篇的文章為例：
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
## 連結顏色更改：
+ 點選 <font color=#E86D2D>themes/next/source/css/_common/components/post/post-body.styl</font>，新增以下語法：
{% codeblock %}
 .post-body 
    a:not(.btn){
      color:rgb(92, 97, 162); //說明：文字本身顏色
      border-bottom: underline;
      &:hover {
        color:rgb(188, 119, 189);  //說明：滑鼠放上後的文字顏色
        text-decoration: underline;
      }
    }
{% endcodeblock %}


## 閱讀全文：
+ 可以縮短文章顯示於首頁的行數（我通常只會顯示2~3行），首頁會出現「閱讀全文」的按鈕，想看更多內容再點入即可，語法為： {% codeblock %}<!-- more --> {% endcodeblock %}
+ 以我某一篇文章的語法為例，<font color=#4287B5>只有在「此語法上方的內容」才會在首頁顯示出來</font>，代表會顯示在首頁上的只會有以下資訊：
>搭乘航空：荷蘭皇家航空
>總飛行時間：1 小時 45 分鐘
>機場：史基浦機場 -> 維也納機場

  {% codeblock %}
  >搭乘航空：荷蘭皇家航空
  >總飛行時間：1 小時 45 分鐘
  >機場：史基浦機場 -> 維也納機場
  <!-- more -->

  ### 史基浦機場：
  **<font color=#909497>比起飛時間提早2.5hr抵達</font>**
  + <font color=#D1756F>準備離境</font> 
  {% endcodeblock %}

### 修改點選「閱讀全文」按鈕後，文字的顯示：
+ 點選 <font color=#E86D2D>themes/next/layout/_macro/post.njk</font>，找到以下語法：<font color=#909497>(快速搜索：mac 的話可以點command+F，windows 的話可以點control+F)</font>
+ 修改前：點開「閱讀全文」後，文章會從閱讀全文按鈕的後續文字開始顯示。
 ``` 
<a class="btn" href="{{ url_for(post.path) }}#more" rel="contents">
 ``` 

+ 修改後：文章會從頂部開始顯示。 <font color=#4287B5>（（（ 差別：刪除 #more"</font>
 ``` 
<a class="btn" href="{{ url_for(post.path) }}" rel="contents">
 ``` 

### 更改閱讀全文的樣式：
+ 點選 <font color=#E86D2D>themes/next/source/css/main.styl</font>，於內部新增下列語法：
 ``` 
//閱讀全文-鼠標放上前的顏色
.post-button .btn {
    color: #424242!important;  //說明：文字顏色
    background-color:rgb(225, 197, 186);  //說明：背景顏色
    font-size: 13px;   //說明：字體大小
    border-radius: 9px 9px 9px 9px;  //說明：圓弧幅度
}

//閱讀全文-鼠標放上後的顏色
.post-button .btn:hover{
  color: #424242!important;    //說明：文字顏色
  background:rgb(229, 218, 121);   //說明：背景顏色
} 
 ``` 

## 文章顯示更新時間：
+ 點選 <font color=#E86D2D>「_config.next.yml」</font>，搜尋<font color=#E86D2D>「post_meta」</font>。
+ 修改前：
 ``` 
post_meta:
  item_text: true
  created_at: true
  updated_at:
    enable: false
    another_day: false
 ``` 
+ 修改 updated_at：<font color=#4287B5>(( 將enable 改成 true</font>
 ``` 
  updated_at:
    enable: true
    another_day: true
 ``` 
+ 使用時：在文章上方加入「updated」的欄位 <font color=#4287B5>(( 第四行</font>
 ``` 
---
title: 【 架網站-6 】hexo的NexT主題：文章內文篇
date: 2024-10-30 18:00:23
updated: 2024-11-30 18:00:23
tags:
  - 從零開始架設部落格
categories: 
  - 🌴 從零開始架設部落格-新手小白的學習筆記
---
 ``` 

## 側欄-目錄：
### 無法顯示標題全文、標題前有數字
+ 點選 <font color=#E86D2D>「_config.next.yml」</font>，搜尋<font color=#E86D2D>「toc」</font>。
+ 修改前：目錄如果標題太長，字會被卡掉、標題前有數字
 ``` 
toc:
  enable: true
  # Automatically add list number to toc.
  number: true
  # If true, all words will placed on next lines if header width longer then sidebar width.
  wrap: false
 ``` 
+ 修改：把「number」改成 false、「wrap」改成 true
 ``` 
toc:
  enable: true
  # Automatically add list number to toc.
  number: false
  # If true, all words will placed on next lines if header width longer then sidebar width.
  wrap: true
 ``` 

 ## 程式區塊-複製選項 copy_button：
+ 點選<font color=#E86D2D>「_config.next.yml」</font>，搜尋<font color=#E86D2D>「copy_button」</font>，將「enable」設為true即可，這樣大家在點你的程式碼時，點選右上角就可以直接複製，方便使用。
```
  copy_button:
    enable: true
```