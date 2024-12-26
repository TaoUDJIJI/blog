---
title: 【 架網站-8 】hexo的NexT主題：標籤篇（彩色標籤、文章底部標籤、標籤大小）
date: 2024-10-30 18:00:25
updated: 2024-10-30 18:00:25
tags:
  - 從零開始架設部落格
categories: 
  - 🌴 從零開始架設部落格-新手小白的學習筆記
---
> 將彩色標籤放到首頁、文章底部-標籤顏色、文章底部-標籤樣式、標籤頁面-調整標籤的大小

<!-- more -->

## 將彩色標籤放到首頁：
+ STEP1：在<font color=#E86D2D>/themes/next/layout/</font>目錄下，新增<font color=#E86D2D>tag-color.nlk</font>文件，新增完成後在文件內加入下方語法：
 ``` 
<script type="text/javascript">
     var alltags = document.getElementsByClassName('tag-cloud-tags');
     var tags = alltags[0].getElementsByTagName('a');
     for (var i = tags.length - 1; i >= 0; i--) {
       var r=Math.floor(Math.random()*75+130);
       var g=Math.floor(Math.random()*75+100);
       var b=Math.floor(Math.random()*75+80);
       tags[i].style.background = "rgb("+r+","+g+","+b+")";
     }
</script>

<style>
  .tag-cloud-tags{
    /*font-family: Helvetica, Tahoma, Arial;*/
    /*font-weight: 100;*/
    text-align: center;
    counter-reset: tags;
  }
  .tag-cloud-tags a{
    border-radius: 6px;
    padding-right: 5px;
    padding-left: 5px;
    margin: 8px 5px 0px 0px;
  }
  .tag-cloud-tags a:before{
  }

  .tag-cloud-tags a:hover{
     box-shadow: 0px 5px 15px 0px rgba(0,0,0,.4);
     transform: scale(1.1);
     /*box-shadow: 10px 10px 15px 2px rgba(0,0,0,.12), 0 0 6px 0 rgba(104, 104, 105, 0.1);*/
     transition-duration: 0.15s;
  }
</style>
 ``` 

+ STEP2：於<font color=#E86D2D>/themes/next/layout/page.nlk/ </font>頁面新增下列語法：
 ``` 
 {% include ' tag-color.njk ' %} 
 ``` 

+ STEP3：於<font color=#E86D2D>/themes/next/layout/index.njk</font>頁面，搜尋下列語法：<font color=#909497>(快速搜索：mac 的話可以點command+F，windows 的話可以點control+F)</font>
``` 
{% block content %}
``` 
在其下方新增下列語法：<font color=#4287B5>（可自行調整標籤的顏色、大小）</font>
``` 
<div class="tag-cloud">
    <div class="tag-cloud-tags" id="tags">
    {{ tagcloud({min_font: 16, max_font: 16, amount: 300, color: true, start_color: '#fff', end_color: '#fff'}) }}
    </div>
  </div>
  <br>
  
  {% include 'tag-color.njk' %}
``` 

## 文章底部-標籤顏色：
+ 位置：<font color=#E86D2D>/themes/next/source/css/_schemes/選擇自己的模板/index.styl</font>
``` 
//文章底部標籤
.posts-expand .post-tags a {
  -webkit-box-shadow: 0 1px 3px rgba(0, 0, 0, .12), 0 1px 2px rgba(0, 0, 0, .24);
  -moz-box-shadow: 0 1px 3px rgba(0, 0, 0, .12), 0 1px 2px rgba(0, 0, 0, .24);
  box-shadow: 0 1px 3px rgba(0, 0, 0, .12), 0 1px 2px rgba(0, 0, 0, .24);
  font-family: 'Comic Sans MS', sans-serif;
  transition: .2s ease-out;
  padding: 3px 5px;
  margin: 5px;
  background: #f5f5f5;
  border-bottom: none;
  border-radius: 15px;

  +mobile(){
    padding: 1px 3px;
    font-size: 8px;
  }

  &:hover {
    background: #b77f7f;
    color: #fff;
    -webkit-box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
    -moz-box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
    box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
  }
}
``` 

## 文章底部-標籤樣式：tag_icon
+ 於<font color=#E86D2D>「_config.next.yml」</font>，搜尋<font color=#E86D2D>「tag_icon」</font>，將它改為 true。
``` 
# Use icon instead of the symbol # to indicate the tag at the bottom of the post
tag_icon: true
``` 

## 標籤頁面-調整標籤的大小
+ 於<font color=#E86D2D>「_config.next.yml」</font>，搜尋<font color=#E86D2D>「tagcloud」</font>，可以修改標籤的尺寸，設定最小（min）、最大（max）的尺寸，我是都設一樣的，如果設不一樣的話，標籤內的文章越多字體會越大。
``` 
# TagCloud settings for tags page.
tagcloud:
  min: 15.5 # Minimum font size in px
  max: 15.5 # Maximum font size in px
  amount: 200 # Total amount of tags
  orderby: name # Order of tags
  order: 1 # Sort order
``` 