# swipebox
swipebox灯箱(仿微博九宫格图片展示效果)


使用方法

将下载的压缩包解压，咱么主要会用到以下文件

    1 src
    2 ├── css
    3 │   ├── swipebox.css  #css样式文件，二选一，推荐swipebox.min.css，文件更小
    4 │   └── swipebox.min.css
    5 ├── img #这个目录的东需全部需要，放到你项目静态目录的根目录下
    6 │   ├── icons.png
    7 │   ├── icons.svg
    8 │   └── loader.gif
    9 └── js #实现动态效果的js代码，二选一，推荐第二个
    10 ├── jquery.swipebox.js
    11    └── jquery.swipebox.min.js
和

    1 lib
    2 └── jquery-2.1.0.min.js # 重要，必须是这个版本的jq，最新版无效
    
开始你的代码

    1 <!DOCTYPE html>
    2 <html lang="en">
    3 <head>
    4 <!-- 脚本及样式文件（根据你文件的具体地址）-->
    5 <script src="/static/js/jquery-2.1.0.min.js"></script>
    6 <script src="/static/js/jquery.swipebox.min.js"></script>
    7 <link rel="stylesheet" href="/static/css/swipebox.min.css">
    8 <meta charset="UTF-8">
    9 <title>测试效果</title>
    10   </head>
    11 <body>
    12   <div class="swipeboxEx"> <!--每个 div class="swipeboxEx" 代表一组图片-->
    13       <a  href="/media/big1" class="swipebox">  <!-- 点击图片后全屏放大的图片-->
    14         <img src="/media/small1" alt="image">  <!-- 直接显示的图片-->
    15       </a> <!-- 每对a标签代表一张大小图-->
    16   </div>
    17   <!--多组图片写多个 div class="swipeboxEx" -->
    18
    19   <!-- 直接复制-->
    20   <script type="text/javascript">
    21      ;( function( $ ) {
    22      $( '.swipebox' ).swipebox();
    23     } )( jQuery );
    24   </script>
    25 </body>
    26</html>

最后说一点，先引用jq的js文件，后引用swipebox的，而且jq的文件必须是作者自带的！！
