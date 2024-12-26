---
title: 【 架網站-4 】hexo的NexT主題：側欄篇（版面配置、新增「關於、標籤、分類」的頁面）
date: 2024-10-30 18:00:21
updated: 2024-10-30 18:00:21
tags:
  - 從零開始架設部落格
categories: 
  - 🌴 從零開始架設部落格-新手小白的學習筆記
---
>側欄：更換位置、更換圖標、新增欄位

>文章：新增標籤（tags）、分類（categories）的資訊
<!-- more -->

## 更改側欄位置：sidebar
+ 點選<font color=#E86D2D>「_config.next.yml」</font>，搜尋<font color=#E86D2D>「sidebar」</font><font color=#909497>(快速搜索：mac 的話可以點command+F，windows 的話可以點control+F)</font>，原先預設是左側，我改成右側。
{% codeblock %}
sidebar:
  # Sidebar Position.
  position: right
{% endcodeblock %}

## 側欄-新增欄位：搜尋
+ **STEP1：在「終端機」輸入下方語法，安裝套件**
{% codeblock %}
npm install hexo-generator-searchdb
{% endcodeblock %}
+ **STEP2：在<font color=#E86D2D>「_config.yml 」</font>新增下方語法**
{% codeblock %}
search:
  path: search.xml
  field: post
  content: true
  format: html
{% endcodeblock %}
+ **STEP3：點開<font color=#E86D2D>「_config.next.yml」</font>**
搜尋<font color=#E86D2D>「local_search」</font>，將「enable」後面改成：true。
{% codeblock %}
local_search:
  enable: true
{% endcodeblock %}

## 側欄-新增欄位：關於(about)、標籤(tags)、分類(categories)
+ 點選<font color=#E86D2D>「_config.next.yml」</font>，搜尋<font color=#E86D2D>「menu」</font>。
+ 語法：<font color=#4287B5>（（若要啟用該項欄位，要先將文字前方的「＃」刪除</font>，我是只有啟用前面五個，啟用後長這樣，<font color=#4287B5>有些要「新增頁面」才可使用哦。</font>
 
  {% codeblock %}
  menu:
    home: / || fa fa-home
    about: /about/ || fa fa-user
    tags: /tags/ || fa fa-tags
    categories: /categories/ || fa fa-th
    archives: /archives/ || fa fa-archive
    #schedule: /schedule/ || fa fa-calendar
    #sitemap: /sitemap.xml || fa fa-sitemap
    #commonweal: /404/ || fa fa-heartbeat
  {% endcodeblock %}

#### <font color=#4287B5>新增頁面-關於(about)、標籤(tags)、分類(categories) </font>
+ **STEP1：在終端機分別輸入以下指令，建立about、tags、categories的頁面**
  {% codeblock %}
  hexo new page about
  {% endcodeblock %}

  {% codeblock %}
  hexo new page categories
  {% endcodeblock %}

  {% codeblock %}
  hexo new page tags
  {% endcodeblock %}

+ **STEP2：點入已新增頁面的「index.md」檔案，編輯頁面內容，tags、categories 兩者要分別在頁面上方輸入「type: tags」、「type: categories」才算啟用完成，about則不需要。**

  {% codeblock %}
  ---
  title: tags
  date: 2024-03-04 10:55:17
  type: tags
  ---
  {% endcodeblock %}

  {% codeblock %}
  ---
  title: categories
  date: 2024-03-04 12:19:22
  type: categories
  ---
  {% endcodeblock %}

#### <font color=#4287B5>將文章加上標籤(tags)、分類(categories)：</font>
+ 以下舉我其中一篇文章為例，要在最上面加上「tags」、「categories」的欄位。
+ 「tags」：是平行階層，如果一次將同一篇文章新增好幾個標籤，會併排顯示，實際效果可以點選我側欄的標籤頁。
+ 「categories」：是上下階層，不支持同級的多項類別，先列的會在上位階，例如這篇文章是分類於「🥥 英國（倫敦）」篇，隸屬於「🌴 旅遊體驗分享-目前皆為自助遊」內，實際效果可以點選我側欄的分類頁。
+ 語法：
{% codeblock %}
---
title: 【倫敦-景點】Frameless Immersive Art Experience
date: 2024-11-1 00:00:15
updated: 2024-11-1 00:00:15
tags:
  - 倫敦-景點
  - 會再訪
categories: 
  - 🌴 旅遊體驗分享-目前皆為自助遊
  - 🥥 英國（倫敦） 
---
{% endcodeblock %}

## 側欄-更改圖標：
#### 更改「側欄上方」的圖標：
點選<font color=#E86D2D>「_config.next.yml」</font>，搜尋<font color=#E86D2D>「menu」</font>。
+ 語法：
{% codeblock %}
menu:
  home: / || fa fa-home
  about: /about/ || fa fa-user
  tags: /tags/ || fa fa-tags
  categories: /categories/ || fa fa-th
  archives: /archives/ || fa fa-archive
  #schedule: /schedule/ || fa fa-calendar
  #sitemap: /sitemap.xml || fa fa-sitemap
  #commonweal: /404/ || fa fa-heartbeat
{% endcodeblock %}

+ 說明：
fa fa-home、fa fa-user、fa fa-tags、fa fa-th、fa fa-archive，這些都是圖標的語法，可以自行替換，這種圖標叫fontawesome，[fontawesome官網](https://fontawesome.com/v6/search?o=r&m=free)還有很多免費圖標可以用哦，不需要登入就可以查詢。

#### 更改「側欄下方」的圖標（作者欄位）：
一樣在<font color=#E86D2D>「_config.next.yml」</font>，搜尋<font color=#E86D2D>「social」</font>。
+ 語法： <font color=#4287B5>（（ 若要啟用該項欄位，要先將文字前方的「＃」刪除</font>
{% codeblock %}
social:
  #GitHub: https://github.com/yourname || fab fa-github
  #E-Mail: mailto:yourname@gmail.com || fa fa-envelope
  #Weibo: https://weibo.com/yourname || fab fa-weibo
  #Twitter: https://twitter.com/yourname || fab fa-twitter
  #FB Page: https://www.facebook.com/yourname || fab fa-facebook
  #StackOverflow: https://stackoverflow.com/yourname || fab fa-stack-overflow
  #YouTube: https://youtube.com/yourname || fab fa-youtube
  #Instagram: https://instagram.com/yourname || fab fa-instagram
  #Skype: skype:yourname?call|chat || fab fa-skype
{% endcodeblock %}
+ 說明：網址可以修改為你自己的社交帳號網址