# 2D转换

## 基本概念

- css3提供了`transform`属性来处理盒子（html标签）的转换，包含位移、旋转、缩放、倾斜等转换。
- 2d转换一般会和过渡transition配合使用。
- 特点：转换后不会影响其他元素
- 注意：2d转换针对行内元素没有效果，针对块级元素和行内块级元素才有效

## 位移 translate(x轴移动量，Y轴移动量);

- 通过translate来设置盒子的位移

- 语法：

    ```css
    基本用法
    tansform : translate(x轴移动量，Y轴移动量);
    tansform : translate(x轴移动量);
    tansform : translateX();
    tansform : translateY();
    例子：
    transform : translate(100px,50px);  //X轴向右移动100px，Y轴向下移动50px
    ```
    
    - 盒子以原来的位置为起点，进行移动
    - 可以设置负值

## 旋转rotate(旋转角度)；

- 通过rotate来设置盒子的2d旋转

- 语法：

    ```css
    语法：
    transform : rotate(旋转角度)；    
    例子：
    transform :  rotate(30deg);  	//盒子以自身中心点为基点，顺时针沿轴旋转30度
    
    x轴旋转：
    transform :  rotateX(30deg);    //盒子以自身中心点为基点，顺时针沿x轴旋转30度
    
    Y轴旋转：
    transform :  rotateY(30deg); 	 //盒子以自身中心点为基点，顺时针沿y轴旋转
    ```

## 缩放scale（宽度的倍数，高度的倍数）;

- 通过scale可以控制盒子的缩放

- 语法：

    ```css
    transform：scale（宽度的倍数，高度的倍数）;
    transform：scale（倍数）;	//等比缩放
    
    例子：
    transform：scale（1.1，1.3）;
    ```
    
    - 取值为数字，1代表1倍，和原尺寸一样，小数会缩小，大于1的数会放大
    - 默认参考中心点

## 倾斜skew(角度); 

- 通过skew属性进行盒子沿着x轴或者y轴进行倾斜转换

- 语法：

    ```css
    transform : skew(角度); 
    
    例子：
    transform : skew(45deg);	//沿着x轴进行倾斜45deg
    transform : skewX(45deg);	//沿着x轴进行倾斜45deg
    transform : skewY(45deg);	//沿着y轴进行倾斜45deg
    ```
    
    - 角度越大，越接近x轴或者y轴，当角度为90deg的时候，会x轴或者y轴平行，消失不见。

## 转换的基点

- 基点就是2D转换时参考的点，通过`transform-origin`来控制参考点

- 语法：

    ```css
    transform-origin:x y;
    x代表x轴上的取值，y代表y轴上的取值
    ```

    - 单词：left right  top  bottom  center   默认是center center，默认盒子是按照中心点进行转换
    - 像素
    - 百分比

- 注意：

    - **转换的基点需要在转换之前确定**，否则浏览器解析会出问题
    - 转换基点，针对位移是没有效果的，因为位移是参考原来的位置进行移动
    - 针对于缩放和旋转以及倾斜是有效果的，因为这两个是参考点进行变换，默认参考中心点，改变了基点，效果也会发生变化

## 2D转换的组合使用

- 概念：多个2D转换组合在一起，每个转换都能作用

- 每种转换之间使用空格隔开

- 注意：旋转会改变x轴和y轴的方向，会影响位移的方向；使用过程中根据需要，确定是先旋转还是先位移

    ```css
    例子：
    /* 水平移动200px ，并且旋转45deg */
    /*位移  缩放  倾斜  旋转*/
    transform: translateX(200px) rotate(45deg);
    ```

### 练习

​	导航栏-2D

​	![image-20200916195557723](https://woniumd.oss-cn-hangzhou.aliyuncs.com/web/longzongfei/20210628145719.png)

```
<style>
        body{
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #f8f8f8;
        }
        nav{
            display: flex;
        }
       a{
           display: block;
           width: 150px;
           height: 40px;
           font-size: 30px;
           font-weight: 600;
           color: gray;
           text-decoration: none;
           line-height: 40px;
           text-align: center;
           position: relative;
       }
       a::after{
           content: "";
           display: block;
           width: 100%;
           height: 3px;
           background-color: #4c81c9;
           position: absolute;
           top: 50px;
           left: 0;
           transform: scale(0);
           transition: 0.6s linear;
       }
       a:hover{
           color:#4c81c9;
       }
       a:hover::after{
           transform: scale(1);
       }
       
    </style>

    <nav>
        <a href="">关于我们</a>
        <a href="">产品介绍</a>
        <a href="">公司介绍</a>
    </nav>
```

**照片墙**

![image-20201226120622143](https://woniumd.oss-cn-hangzhou.aliyuncs.com/web/longzongfei/20210628145723.png)

```
<style>
    body{
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #f1f1f1;
        height: 100vh;
    }
    .box{
        width: 600px;
        height: 700px;
        border: 1px solid #cccccc;
        position: relative;
        border-radius: 5px;
    }
    .box .item{
        width: 100%;
        height: 100%;
        background-color: white;
        box-shadow: 2px 2px 10px 0px rgba(0,0,0,0.7);
        position: absolute;
        top: 0;
        left: 0;
        border-radius: 5px;
        transition: all 1s;

    }
    .box .item .img{
        width: 90%;
        height: 80%;
        margin: 5%;
        background:url("img/gyy01.jpeg") center center no-repeat;
        background-size: cover; 
        opacity: 0.75;
        transition: all 1s;
    }
    .box .item-2 .img{
        background-image: url("img/gyy02.jpeg");
    }
    .box .item-3 .img{
        background-image: url("img/gyy03.jpg");
    }
    .box .item p{
        height: 20%;
        font-size: 30px;
        text-align: center;
        margin: 0;
    }
    .box .item-1 {

        transform: translate(5%,-10%) scale(0.4) rotate(-5deg);
    }
    .box .item-2 {
        transform: translate(-10%,10%) scale(0.4) rotate(-1deg);
        z-index: 2;
    }
    .box .item-3{
        transform: translate(20%,20%) scale(0.4) rotate(-4deg);
        z-index: 1;
    }
    .box .item:hover{
        transform: scale(1);
        z-index: 5;

    }
    .box .item:hover .img{
        opacity: 1;
    }
</style>

<div class="box">
    <div class="item item-1">
        <div class="img"> </div>
        <p>北京</p>
    </div>
    <div class="item item-2">
        <div class="img"> </div>
        <p>北京</p>
    </div>
    <div class="item item-3">
        <div class="img"> </div>
        <p>北京</p>
    </div>
</div>
```

