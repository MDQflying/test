#三栏布局（flex,table,position,）



##圣杯布局
基础HTML

~~~
<body>
    <div class="container">
        <!-- 优先渲染 -->
        <div class="center">
            center
        </div>
        <div class="left">
            left
        </div>
        <div class="right">
            right
        </div>
    </div>
</body>
~~~
基础CSS

~~~

  .container {
        overflow: hidden;
    }
    .container > div {
        position: relative;
        float: left;
        height: 100px;
    }
    .center {
        width: 100%;
        background-color: red;
    }
    .left {
        width: 200px;
        background-color: green;
    }
    .right {
        width: 200px;
        background-color: blue;
    }
~~~


##Flex 布局

基础HTML

~~~
<div class="container">
    <!-- 优先渲染 -->
    <div class="center">center</div>
    <div class="left">left</div>
    <div class="right">right</div>
  </div>
~~~
基础CSS

~~~
.container {
  display: flex;
  height: 300px;
}
.center {
  background-color: red;
  width: 100%;
  order: 2;
}
.left {
  background-color: green;
  width: 200px;
  flex-shrink: 0;
  order: 1;
}
.right {
  background-color: blue;
  width: 200px;
  flex-shrink: 0;
  order: 3;
}
~~~
##Table 布局