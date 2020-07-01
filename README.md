# rotate_photo

## 效果图


## 步骤
### 准备
先准备12张图片备用（也可以是6张），放到images文件夹中
![相册图片准备](/photo_img.png)

### 文件结构

![文件结构]()

#### css
css文件夹：index.css
```
body, div, img {
  margin: 0;
  padding: 0;
}
body {
  width: 100%;
  height: 600px;
  background: linear-gradient(#fb3 20%, #58a 80%);
}
.cude {
  width: 200px;
  height: 200px;
  margin: 200px auto;
  transform-style: preserve-3d;
  animation: rotate 20s infinite;
  animation-timing-function: linear;
}
.cude .cude-out {
  width: 200px;
  height: 200px;
  position: relative;
}
.cude-out div{
  width: 200px;
  height: 200px;
  position: absolute;
  transition: all .4s;
}
.cude-out div img {
  width: 200px;
  height: 200px;
}
@keyframes rotate {
  from {
    transform: rotateX(0deg) rotateY(0deg);
  }
  to {
    transform: rotateX(360deg) rotateY(360deg);
  }
}
.cude-out .out-font {
  transform: translateZ(100px);
  background: #9ccd63;
}
.cude-out .out-back {
  transform: translateZ(-100px);
  background: #ddce4a;
}
.cude-out .out-left {
  transform: rotateY(90deg) translateZ(100px);
  background: #00FFFF;
}
.cude-out .out-right {
  transform: rotateY(-90deg) translateZ(100px);
  background: #0000FF;
}
.cude-out .out-top {
  transform: rotateX(90deg) translateZ(100px);
  background: #00FF00;
}
.cude-out .out-bottom {
  transform: rotateX(-90deg) translateZ(100px);
  background: #5e6166;
}
.cude .cude-in {
  top: 50px;
  left: 50px;
  width: 100px;
  height: 100px;
  position: absolute;
}
.cude-in div {
  width: 100px;
  height: 100px;
  position: absolute;
}
.cude-in img {
  width: 100px;
  height: 100px;
}
.cude-in .in-font {
  transform: translateZ(50px);
}
.cude-in .in-back {
  transform: translateZ(-50px);
}
.cude-in .in-left {
  transform: rotateY(90deg) translateZ(50px);
}
.cude-in .in-right {
  transform: rotateY(-90deg) translateZ(50px);
}
.cude-in .in-top {
  transform: rotateX(90deg) translateZ(50px);
}
.cude-in .in-bottom {
  transform: rotateX(-90deg) translateZ(50px);
}

/*鼠标悬浮在外立方体散开*/
.cude:hover .cude-out .out-font {
  transform: translateZ(200px);
}
.cude:hover .cude-out .out-back {
  transform: translateZ(-200px);
}
.cude:hover .cude-out .out-left {
  transform: rotateY(90deg) translateZ(200px);
}
.cude:hover .cude-out .out-right {
  transform: rotateY(-90deg) translateZ(200px);
}
.cude:hover .cude-out .out-top {
  transform: rotateX(90deg) translateZ(200px);
}
.cude:hover .cude-out .out-bottom {
  transform: rotateX(-90deg) translateZ(200px);
}

/*鼠标悬浮在内立方体散开*/
.cude:hover .cude-in .in-font {
  transform: translateZ(100px);
}
.cude:hover .cude-in .in-back {
  transform: translateZ(-100px);
}
.cude:hover .cude-in .in-left {
  transform: rotateY(90deg) translateZ(100px);
}
.cude:hover .cude-in .in-right {
  transform: rotateY(-90deg) translateZ(100px);
}
.cude:hover .cude-in .in-top {
  transform: rotateX(90deg) translateZ(100px);
}
.cude:hover .cude-in .in-bottom {
  transform: rotateX(-90deg) translateZ(100px);
}
```

#### html
html：index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>旋转相册</title>
  <link rel="stylesheet" href="css/index.css">
</head>

<body>
  <div class="cude">
    <!--外立方体-->
    <div class="cude-out">
      <div class="out-font">
        <img src="images/reba-1.jpg" alt="">
      </div>
      <div class="out-back">
        <img src="images/reba-2.jpg" alt="">
      </div>
      <div class="out-left">
        <img src="images/reba-3.jpg" alt="">
      </div>
      <div class="out-right">
        <img src="images/reba-4.jpg" alt="">
      </div>
      <div class="out-top">
        <img src="images/reba-5.jpg" alt="">
      </div>
      <div class="out-bottom">
        <img src="images/reba-6.jpg" alt="">
      </div>
    </div>
    <!--内立方体-->
    <div class="cude-in">
      <div class="in-font">
        <img src="images/reba-1.jpg" alt="">
      </div>
      <div class="in-back">
        <img src="images/reba-2.jpg" alt="">
      </div>
      <div class="in-left">
        <img src="images/reba-3.jpg" alt="">
      </div>
      <div class="in-right">
        <img src="images/reba-4.jpg" alt="">
      </div>
      <div class="in-top">
        <img src="images/reba-5.jpg" alt="">
      </div>
      <div class="in-bottom">
        <img src="images/reba-6.jpg" alt="">
      </div>
    </div>
  </div>
</body>
</html>
```


