---
title: 【 架網站-5 】hexo的NexT主題：個人資訊篇（首頁圖片、作者圖片、網站圖標）
date: 2024-10-30 18:00:22
updated: 2024-10-30 18:00:22
tags:
  - 從零開始架設部落格
categories: 
  - 🌴 從零開始架設部落格-新手小白的學習筆記
---
>包含首頁圖片、作者圖片、網站圖標
<!-- more -->

## 新增首頁照：custom logo
+ Step1：將圖片上傳至<font color=#E86D2D>/theme/next/source/images</font>中，以我為例，我將圖片名稱取為「custom-logo pig TAO UD draw.png」。

+ Step2：點選<font color=#E86D2D>「_config.next.yml」</font>，搜尋<font color=#E86D2D>「custom_logo」</font>，以修改圖片的路徑。

  原本是這樣：
  {% codeblock %}
  # Custom Logo (Warning: Do not support scheme Mist)
  custom_logo: #/uploads/custom-logo.png
  {% endcodeblock %}
  我改成：<font color=#4287B5>（custom_logo:後方的＃記得要刪掉，才能啟用該圖片）</font>
  {% codeblock %}
  # Custom Logo (Warning: Do not support scheme Mist)
  custom_logo: /images/custom-logo pig TAO UD draw.png
  {% endcodeblock %}


## 新增作者圖片：avatar
+ Step1：將圖片上傳至<font color=#E86D2D>/theme/next/source/images</font>中，以我為例，我將圖片名稱取為「avatar-bear TAO UD draw.png」。

+ Step2：點選<font color=#E86D2D>「_config.next.yml」</font>，搜尋<font color=#E86D2D>「avatar」</font>，以修改圖片的路徑，還可以選擇照片邊框是否要圓形、是否要旋轉。

  原本是這樣：
  {% codeblock %}
  # Sidebar Avatar
  avatar:
  # Replace the default image and set the url here.
  url: #/images/avatar.gif
  # If true, the avatar will be displayed in circle.
  rounded: false
  # If true, the avatar will be rotated with the cursor.
  rotated: false
  {% endcodeblock %}

  我改成：<font color=#4287B5>（差別在第四行、第六行。第四行 url：後方的＃記得要刪掉，才能啟用該圖片，）</font>
  {% codeblock %}
  # Sidebar Avatar
  avatar:
  # Replace the default image and set the url here.
  url: /images/avatar-bear TAO UD draw.png
  # If true, the avatar will be displayed in circle.
  rounded: true
  # If true, the avatar will be rotated with the cursor.
  rotated: false
  {% endcodeblock %}

## 設置網站圖標：favicon
+ Step1：可以查看看「Favicon圖示產生器」，有的可將自有圖檔轉換為32*32的圖標，圖標用好後上傳至<font color=#E86D2D> /theme/next/source/images </font>中，以我為例，我將圖片名稱取為「favicon-icecream-32x32.png」。

+ Step2：點選<font color=#E86D2D>「_config.next.yml」</font>，搜尋<font color=#E86D2D>「favicon」</font>。

  原本是這樣：
  {% codeblock %}
  favicon:
  small: /images/bear_black.png
  medium: /images/bear_black.png
  apple_touch_icon: /images/bear_black.png
  safari_pinned_tab: /images/bear_black.png
  {% endcodeblock %}

  我改成：<font color=#4287B5>（圖片換成我自己畫的插畫）</font> 
  {% codeblock %}
  favicon:
  small: /images/favicon-icecream-32x32.png
  medium: /images/favicon-icecream-32x32.png
  apple_touch_icon: /images/favicon-icecream-32x32.png
  safari_pinned_tab: /images/favicon-icecream-32x32.png
  {% endcodeblock %}


+ Step3：如果使用「hexo clean」清除緩存後，圖標仍然沒有更新的話，可以試試「清除所有瀏覽記錄」。