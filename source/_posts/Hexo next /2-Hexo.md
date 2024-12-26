---
title: 【 架網站-2 】從「網頁框架平台-hexo」選擇網頁的主題樣式
date: 2024-10-30 18:00:19
updated: 2024-10-30 18:00:19
tags:
  - 從零開始架設部落格
categories: 
  - 🌴 從零開始架設部落格-新手小白的學習筆記

---
>hexo：是靜態網站的網頁框架平台，有很多種主題可以自己選擇喜歡的版型，但選擇上要注意是否還有成員在做後續維護。
<!-- more -->

## hexo 的主題：
+ [官網](https://hexo.io/themes/)：裡面有很多主題模板，我是選擇「NexT」主題，版面比較簡約，畢竟第一次架網站，想說先選個不複雜的，而且會選它很重要的一點是有成員在做後續維護。

## 「NexT」主題：
>[官網有教學](https://theme-next.js.org/docs/getting-started/)：可以選擇透過 npm 安裝，或是選擇 git 安裝，我是選擇 git ，以下都以 git 爲介紹。
+ **Step1：在終端機上複製該命令，將NexT的主題下載到電腦上**
{% codeblock %}
git clone https://github.com/next-theme/hexo-theme-next themes/next
{% endcodeblock %}

+ **Step2：建立NexT主題的設定檔：「_config.next.yml」**
如果您是第一次安裝 NexT 主題，可以執行以下命令以取得可用的 NexT 設定檔：
{% codeblock %}
cp themes/next/_config.yml _config.next.yml
{% endcodeblock %}

+ **Step３：啟用 NexT**
打開「Visual Studio Code」<font color=#909497> (這是我為了寫程式方便下載的，各位自行考慮要不要用這個)</font>，點選左側<font color=#E86D2D>「_config.yml」</font>名稱的資料夾，將「theme」修改為「next」，打開終端機，啟動hexo server (可以簡打「hexo s」)，主題套用完成。

+ **Step4：進一步選擇「NexT」的主題模板**
 1. 目前有四種，分別為 Muse、Mist、Pisces、Gemini，我是選擇Gemini，全憑個人喜好。[官網](https://github.com/next-theme/hexo-theme-next)有附上不同模板的網頁連結，可以點開參考。
 2.	Pisces、Gemini 的差別：一開始我是選 Pisces ，開始寫文章後發現首頁的文章都是連在一起的，我不太喜歡，所以後來換成 Gemini，首頁的每篇文章就有區隔開來。
 3. 確定好想要哪個後，從<font color=#E86D2D>「_config.next.yml」</font>修改主題模板，搜尋「Schemes」<font color=#909497>(快速搜索：mac 的話可以點command+F，windows 的話可以點control+F)</font>，想要套用哪個模板就把它前面的#去掉就行。
{% codeblock %}
 #scheme: Muse
 #scheme: Mist
 #scheme: Pisces
 #scheme: Gemini
{% endcodeblock %}
