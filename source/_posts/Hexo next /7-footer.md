---
title: 【 架網站-7 】hexo的NexT主題：頁尾篇（作者圖標、訪客統計、版權聲明、贊助按鈕）
date: 2024-10-30 18:00:24
updated: 2024-10-30 18:00:24
tags:
  - 從零開始架設部落格
categories: 
  - 🌴 從零開始架設部落格-新手小白的學習筆記
---
>作者圖標、訪客統計、版權聲明、放上贊助按鈕
<!-- more -->

## 首頁的頁尾
### 作者圖標：icon name
+ 點選 <font color=#E86D2D>「_config.next.yml」</font>，搜尋<font color=#E86D2D>「icon」</font><font color=#909497>(快速搜索：mac 的話可以點command+F，windows 的話可以點control+F)</font>。
+ 「fa fa-heart」指的是愛心，可以自己替換成喜歡的圖標，這種圖標叫fontawesome，[fontawesome官網](https://fontawesome.com/v6/search?o=r&m=free)還有很多免費圖標可以用哦，不需要登入就可以查詢。原本預設是一顆正紅色的愛心，我是只有把顏色改成粉色。
 ```
   icon:
    # Icon name in Font Awesome. See: https://fontawesome.com/icons
    name: fa fa-heart
    # If you want to animate the icon, set it to true.
    animated: false
    # Change the color of icon, using Hex Code.
    color: "#EB716A"
 ```

### 訪客統計：busuanzi_count
+ 點選 <font color=#E86D2D>「_config.next.yml」</font>，搜尋<font color=#E86D2D>「busuanzi_count」</font>。
+ 以下語法為系統預設，想顯示訪客統計的話，將「enable」修改為「true」即可。<font color=#4287B5>（（下方第二行））</font> 這邊跟上面一樣可以自己改圖標哦～
 ```
busuanzi_count:
  enable: false
  total_visitors: true
  total_visitors_icon: fa fa-user
  total_views: true
  total_views_icon: fa fa-eye
  post_views: true
  post_views_icon: far fa-eye
```

## 文章內的頁尾
### 自定義文章版權聲明：creative_commons
+ 點選 <font color=#E86D2D>「_config.next.yml」</font>，搜尋<font color=#E86D2D>「creative_commons」</font>。
+ 以下語法為系統預設，如果想要在文章頁尾展示出來， 將「post:」的 false 改成 true 即可。<font color=#4287B5>（（下方第七行</font> 
```
creative_commons:
  # Available values: by | by-nc | by-nc-nd | by-nc-sa | by-nd | by-sa | cc-zero
  license: by-nc-sa
  # Available values: big | small
  size: small
  sidebar: false
  post: false
 ```
### 放上抖內/打賞/贊助的按鈕：reward
+ 點選 <font color=#E86D2D>「_config.next.yml」</font>，搜尋<font color=#E86D2D>「reward」</font>。
+ 以下語法為系統預設，如果想要在文章頁尾展示出抖內/打賞/贊助的按鈕， 將「enable:」的 false 改成 true 即可。<font color=#4287B5>（（下方第三行</font> 
 ```
reward_settings:
  # If true, a donate button will be displayed in every article by default.
  enable: false
  animation: false

reward:
  #wechatpay: /images/wechatpay.png
  #alipay: /images/alipay.png
  #paypal: /images/paypal.png
  #bitcoin: /images/bitcoin.png
 ```
 + 開啟成功後發現系統的默認語言文本是「捐贈」，誒都...我覺得怪怪的，所以我把文本改成「抖內支持」。修改文本的詳細內容可參考<font color=#4599B6>【 架網站-3 】hexo的NexT主題：更換顏色篇（背景、頂部、側欄）、選擇網頁語言、修改語言文本內容</font>。

+ 這是我後來修改後的樣子，我選擇另外新增「抖內支持」的網址跟圖片。<font color=#4287B5>（（下方第六行</font> 
 ```
reward:
  #wechatpay: /images/wechatpay.png
  #alipay: /images/alipay.png
  #paypal: /images/paypal.png
  #bitcoin: /images/bitcoin.png
  https://taoudlovesjijibird.bobaboba.me/: /images/bobaboba.png
 ```