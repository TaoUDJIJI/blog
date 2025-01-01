---
title: 【 架網站-1 】網頁背後的秘密-「markdown」常用語法
date: 2024-10-30 18:00:18
updated: 2024-10-30 18:00:18
tags: 從零開始架設部落格
categories: 
  - 🌴 從零開始架設部落格-新手小白的學習筆記
---
>新手小白練習筆記

<!-- more -->

## <font color=#E86D2D>標題篇：</font>
+ ＃的後面要空一格再打字
+ ＃x7無效
+ 因為是標題所以會自動與內文空一行

{% codeblock %}
＃x7無效
# 我是標題 1
## 我是標題 2
### 我是標題 3
#### 我是標題 4
##### 我是標題 5 （大小跟內文差不多，只是變粗）
###### 我是標題 6 (比內文還小)
{% endcodeblock %}

# 我是標題 1
## 我是標題 2
### 我是標題 3
#### 我是標題 4
##### 我是標題 5 （大小跟內文差不多，只是變粗）
###### 我是標題 6 (比內文還小)

## <font color=#E86D2D>顏色篇：</font>
+ 可上網搜尋「HTML顏色代碼」，查詢更多顏色的代碼。
+ 成果：<font color=#6b8e23>軍綠色is me</font> 
{% codeblock %}
<font color=#6b8e23>軍綠色is me</font> 
{% endcodeblock %}
+ 說明：
顏色代碼</font>：<font color=#909497>#6b8e23</font>
打上想要被著色的文字：<font color=#909497>軍綠色is me</font></font>

## <font color=#E86D2D>內文篇：</font>

### 刪除線
+ 成果：~我是刪除線~
{% codeblock %}
~我是刪除線~
{% endcodeblock %}
+ 說明：文字的前後加上兩個波浪號「 ~ 」(是半形不是全形哦)

### 底線
+ 成果：<font> <u>我是底線</u> </font> 
{% codeblock %}
<font> <u>我是底線</u> </font> 
{% endcodeblock %}
 
### 斜體字
+ *我是斜體*
{% codeblock %}
*我是斜體*
{% endcodeblock %}

+ ***我是粗斜體***
{% codeblock %}
***我是粗斜體***
{% endcodeblock %}

+ 說明：
符號是半形不是全形（全形、半形有別，分別為＊、*）

### 粗體字
+ **我是粗體** 
{% codeblock %}
**我是粗體**
{% endcodeblock %}
+ 說明：
符號是半形不是全形（全形、半形有別，分別為＊、*）

### 引言
+ 成果：
>123
>321
>1234567
+ 語法：
{% codeblock %}
>123
>321
>1234567
{% endcodeblock %}
+ 說明：在文字前方輸入「 > 」的符號

### 說話框：
{% cq %} 你好，我好，大家好 {% endcq %}

+ 語法：
 ``` 
 {% cq %} 你好，我好，大家好 {% endcq %}
 ```

### 文字靠左：
<p align="left">我在左邊</p> 
 ``` 
<p align="left">我在左邊</p> 
 ``` 

### 文字置中：
 <center>我在中間</center>
 ``` 
 <center>我在中間</center>
 ``` 


### 文字靠右：
<p align="right">我在右邊</p>
 ``` 
<p align="right">我在右邊</p>
 ``` 


### 程式區塊：
+ 成果：下方灰色方框
+ 語法1：
```
   ```
   文字
   ```   
```

+ 語法2：
 ``` 
 {% codeblock %}
 文字
 {% endcodeblock %}
 ```

### 清單-無序清單(圓點)：
+ 說明：最前面加上「 +（加號）」，符號後面要空一行再打字
#### 單個
+ 恰吉 （此為成果

+ 語法：
{% codeblock %}
+ 恰吉
{% endcodeblock %}

#### 還可以用階層式
+ 恰吉仔
   + 一個恰吉
     + 兩個恰吉

+ 語法：
{% codeblock %}
+ 恰吉仔
   + 一個恰吉
     + 兩個恰吉
{% endcodeblock %}

### 超連結：
+ 成果：[youtube](https://www.youtube.com)
{% codeblock %}
[youtube](https://www.youtube.com)
{% endcodeblock %}

+ 說明：
[  ]：輸入想要顯示的文字
(  )：輸入要連結到的網址

### 箭頭
+ 成果：&uarr;  &darr;  &larr;  &rarr;  &harr;
+ 語法：
 {% codeblock %}
 &uarr;  &darr;  &larr;  &rarr;  &harr;
 {% endcodeblock %}

### 水平虛線分割線：

***

+ 語法1：
 {% codeblock %}
 ***
 {% endcodeblock %}

+ 語法2：
 {% codeblock %}
 ---
 {% endcodeblock %}

### 代辦事項：
- [ ] 代辦事項
- [x] 已完成事項

+ 語法：
 {% codeblock %}
- [ ] 代辦事項
- [x] 已完成事項
 {% endcodeblock %}

### 文字重點標記-1：
今天有`太陽`，心情真好

 ``` 
今天有`太陽`，心情真好
 ``` 
### 文字重點標記-2：
+ STEP1：點選<font color=#E86D2D>「_config.next.yml」</font>，搜尋<font color=#E86D2D>「custom_file_path」</font><font color=#909497>(快速搜索：mac 的話可以點command+F，windows 的話可以點control+F)</font>，把「variable: source/_data/variables.styl」前面的＃刪除，以開啟該項功能。<font color=#4287B5>（（下方第11欄</font>
{% codeblock %}  
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
  {% endcodeblock %}

+ STEP2：在<font color=#E86D2D> source/_data/variables.styl </font>新增以下語法：<font color=#4287B5>（顏色、大小都可以自己調整參數 </font> 
{% codeblock %}  
//自定義文字色塊
span#inline-blue, span#inline-green, span#inline-purple, span#inline-red {
    display: inline;
    padding: .2em .6em .3em;
    font-size: 90%;
    font-weight: 700;
    line-height: 1;
    color: #fff;
    text-align: center;
    vertical-align: baseline;
    border-radius: 0;
    white-space: nowrap;
}
span#inline-blue {
    background-color:rgb(101, 162, 231);
}
span#inline-purple {
    background-color:rgb(171, 121, 196);
}
span#inline-red {
    background-color:rgb(232, 121, 107);
}
span#inline-green {
    background-color: #5cb85c;
}
{% endcodeblock %}

+ STEP3：使用時輸入下列語法：
{% codeblock %}
<span id="inline-blue">內容</span>

<span id="inline-purple">內容</span>

<span id="inline-red">內容</span>

<span id="inline-green">內容</span>
{% endcodeblock %}

+ 成果：

   <span id="inline-blue">內容</span>
  
   <span id="inline-purple">內容</span>

   <span id="inline-red">內容</span>

   <span id="inline-green">內容</span>

### 重點提示框：
+ 先在<font color=#E86D2D> source/_data/variables.styl </font>新增以下語法：<font color=#4287B5>（顏色、大小都可以自己調整參數 </font> 
{% codeblock %}  
//自定義NOTE
.alert {
    padding: 15px;
    margin-bottom: 20px;
    border: 1px solid transparent;
    border-radius: 4px;
}
.alert-green {
    color: rgb(77, 84, 88);
    background-color: #dff0d8;
    border-color: #d6e9c6;
}
.alert-blue {
    color:rgb(77, 84, 88);
    background-color:rgb(225, 239, 247);
    border-color:rgb(187, 215, 229);
}
.alert-yellow {
    color:rgb(77, 84, 88);
    background-color: #fcf8e3;
    border-color: #faebcc;
}
.alert-red {
    color: rgb(77, 84, 88);
    background-color: #f2dede;
    border-color: #ebccd1;
}

{% endcodeblock %}


+ 使用時輸入下列語法：
{% codeblock %}
<div class="alert alert-blue"><i class="fa fa-arrow-circle-right"></i>藍色</div>

<div class="alert alert-yellow"><i class="fa fa-bell"></i>黃色</div>

<div class="alert alert-green"><i class="fa fa-arrow-right"></i>綠色</div>

<div class="alert alert-red"><i class="fa fa-bolt"></i>紅色</div>
{% endcodeblock %}

+ 成果：

<div class="alert alert-blue"><i class="fa fa-arrow-circle-right"></i>藍色</div>

<div class="alert alert-yellow"><i class="fa fa-bell"></i>黃色</div>

<div class="alert alert-green"><i class="fa fa-arrow-right"></i>綠色</div>

<div class="alert alert-red"><i class="fa fa-bolt"></i>紅色</div>

+ 說明：以下這些是圖標的語法。這種圖標叫fontawesome，[fontawesome官網](https://fontawesome.com/v6/search?o=r&m=free)還有很多免費圖標可以用哦，不需要登入就可以查詢。
{% codeblock %}
<i class="fa fa-arrow-circle-right"></i>    //藍框的圖標
<i class="fa fa-bell"></i>                  //黃框的圖標
<i class="fa fa-arrow-right"></i>           //綠框的圖標
<i class="fa fa-bolt"></i>                  //紅框的圖標
{% endcodeblock %}

+ 說明：其他我也很喜歡的圖標：
<i class="fa fa-tree"></i> 、 <i class="fa fa-commenting"></i> 、 <i class="fa fa-exclamation-triangle"></i> 、 <i class="fa fa-long-arrow-right"></i> 、 <i class="fa-regular fa-comment"></i> 、 <i class="fa-solid fa-location-dot"></i> 、 <i class="fa-regular fa-heart"></i>  、 <i class="fa-regular fa-bell"></i> 、 <i class="fa-regular fa-bookmark"></i> 、 <i class="fa-regular fa-thumbs-up"></i> 、 <i class="fa-regular fa-comments"></i> 、 <i class="fa-regular fa-flag"></i> 、 <i class="fa-regular fa-circle-check"></i>、<i class="fa-regular fa-lightbulb"></i> 、 <i class="fa-brands fa-waze"></i> 
<i class="fa-regular fa-key"></i>