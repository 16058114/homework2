## 16058114  廉晨曦 ##


## 1、站点的策划思路
> * 最初我是打算写一个游戏界面的，比如王者荣耀或者英雄联盟，后来在上课期间发现很多同学都写的游戏网页，感觉写这个的太多了，很容易就会重复，于是换了个思路，想写风景之类的东西，然后我就想到了中国的世界遗产，于是就这么定下来了。
> * 水平有限，难以达到期望的效果，但也是尽了最大努力
> * 内容来源[]()http://www.whcn.org/

## 2、页面结构与说明
> * 一个主页，介绍网站主题[]()https://16058114.github.io/homework/
> * 一个自然遗产名录，内容是中国入选的自然遗产
> * 一个文化遗产名录，内容是中国入选的文化遗产
> * 一个站长信息页面
> * 一个注册页面

## 3、技术指标
> * 兼容的浏览器版本：IE8+CHROME+FIREFOX+OPERA+360
> * 版本：HTML5 CSS3
> * 开发软件：webstorm

### 难点1：导航栏的实现
导航栏的关键一方面是排版，另一方面是把li由纵向改为横铺，需要一个float:left，另外还要去掉li前面的符号 list-style:none. 我在百度上找到一个样本，然后分析，修改，完成了自己的导航栏。
```
div
{
        border:1px solid black;
        width:410px;
        height:26px;
        margin-left:30%;
        margin-top:20%;
    }
    .daohang ul  /*导航条ul的样式(不重要)*/
    {
        width:100%;
        height:26px;
        margin:0px;
	padding:0px;/*建议设置，避免出现内间距*/
     }
     .daohang ul li /*(重要)导航条项的样式*/
     {
         margin-left:2px;
         float:left; /*关键地方，li横铺，通常是竖着的*/
         cursor:pointer;
         text-align:center;
         line-height:26px;
         height:26px;
         width:100px;
	 border-style:none;
	 list-style:none;/*必须，取消li前面的符号*/
         border-bottom:1px solid black;
         background-color:#d6d6d6;
     }

```
### 难点2: 轮播图的实现
首页不知道放什么比较合适，想了想还是加一个轮播图比较好，苦思许久，真的不会，百度了一个简易的轮播图，略作修改。勉强算是实现了。以下是代码的一部分。
```
<script>
    var curIndex = 0;
    var auto = setInterval(function () {
        if(curIndex >= $(".imgList li").length -1){
            curIndex = 0;
        }
        else
            curIndex++;
        changeTo(curIndex);
    },2500);
    function changeTo(num) {
        $(".imgList").find("li").removeClass(".imgOn").hide().eq(num).fadeIn().addClass(".imgOn");
    }
</script>
```

### 难点3：排版
不得不说，HTML文件的排版真的是非常重要，一个HTML页面，不管技术手段多么高超，没有好的排版，简直不忍直视。

## 4、开发心得
这次开发就是我第一次实战的过程，过程中出现了许多问题，很可能一个小错误就需要多次检查代码，或者查书，或者百度，或者问同学，到最后也未能完美解决所有问题。总的来说这次网站制作并不算很成功，但是我也是很努力的做了，总之，这个学期还是很有收获的。
