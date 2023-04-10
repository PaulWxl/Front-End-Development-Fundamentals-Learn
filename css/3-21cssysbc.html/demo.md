- 精灵图： 将多个小图片放在一张大图片上，这个大图片就叫精灵图
- 网站的图片都在服务器上（所以难怪是网址的形式），服务器传到浏览器的，放在一张图片上可以减少服务器向浏览器发送的次数，提高浏览器的性能
- 背景图片连写属性
- 颜色 路径 平铺 位置/尺寸
- 注意连写有默认值影响
- 注意尺寸和位置之间有一个/
- 注意位置是九个方向其中的一个（可以理解为主轴，侧轴），
- 注意单写如果要写一定要写在连写的下方，因为连写有默认的样式，不写的话可能会覆盖掉上面的单写，所以要么就在连写里面写，要么就一定在连写的下方写单写
- 尺寸的属性
- background-size
- 数字+px  、   百分比（相对于装这个背景图片的盒子的宽高）  最常用
- contain： 把背景图片等比例放大 一直放大到恰好等于盒子的最大宽高 切记：会有留白
- cover： 在contain的基础上继续放大，最后把整个装它的盒子全部占满，图片会变形，但是，没有留白。
- .fjt-one {
            width: 400px;
            height: 400px;
            margin: 150px auto;
            border: 1px solid pink;
            background:  url(./images/fjt.png) no-repeat center center;
        }
        .fjt-two {
            width: 400px;
            height: 400px;
            margin: 50px auto;
            border: 1px solid pink;
            background: url(./images/fjt.png) no-repeat center center/contain ;

        }
        .fjt-three {
            width: 400px;
            height: 400px;
            margin: 50px auto;
            border: 1px solid pink;
            background: url(./images/fjt.png) no-repeat center center/cover ;

        }
- 精灵图的使用：
- 在pxcook上量取左上角的尺寸，先设置一个装这个图片的盒子，然后把盒子的宽高都设置成跟这个图片的宽高一模一样（在pxcook中量）最后在尺寸那里一定要设置为图片左上角坐标的相反数
- .jlt {
            width: 72px;
            height: 58px;
            /* border: 1px solid #ccc; */
            /* margin: 200px auto; */
            background: #fff url(./images/精灵图.png) no-repeat -408px -28px ;

        }
