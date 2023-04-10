- 版心一般记为.container
- 水平居中+宽度固定(pxcook去测量)
- 配合pxcook使用psd格式的图片
- psd格式的图片一般是专门的设计师人员发过来的
- base.css引入的时候放在最上面，其次是common.css,最后是index.css,如果有iconfont.css,放在base后面common前面。
- base.css: 清楚不同浏览器的默认样式
- common.css: 网页的公共部分样式
## 注意， index.css: 自身特定的样式
- ico图标一般直接放在根目录下



## 项目文件夹的命名规范
- xtx-pc-client: 所有项目相关的文件都保存在这个文件夹下
##  images目录 和 uploads目录 images目录： 一般存放网页固定的图片  uploads目录: 存放网页中会更改的图片，images文件夹和uploads文件夹都是存放图片用的，images是固定的图片，uploads是会变的图片。

## 网页骨架 具体见《网页骨架.png》
# 先改变网页语言:  <html lang="zh-CN">  网页标题：<title>小兔鲜儿-新鲜、惠民、快捷！</title>   网页描述： meta-des 
- <meta 
    name="description" 
    content="小兔鲜儿官网，致力于打造全球最大的食品、生鲜电商购物平台。"
    >
# 网页关键词： meta-kw 
- <meta name="keywords" 
    content="小兔鲜儿,食品,生鲜,服装,家电,电商,购物">


# 接下来引入ico图标:   link:favicon
-     <link rel="shortcut icon" href="favicon.ico" type="image/x-icon">



##  再引入css三个(/四个)文件（称为《外联样式》）（base.css + iconfont.css + common.css + ）



##  为了方便看清，先给container加一个背景色（背景色一般都是用来辅助观察的），最后再去掉 注意，用精灵图时要在pxcook上测量该图标左上角的尺寸，最后用背景图片的url引入精灵图。 background: url(...) 直接在url后面空格写左上角的坐标 -...px -...px 注意 一定要写负值。（这里我没有用精灵图，我用的是iconfont）



## 注意，标签语义化。 头部模块 header语义化标签 注意版心是否包裹其他标签依情况而定. 快捷菜单(shortcut)模块 命名规范：  ...(项目名称，例：xtx)-shortcut。  主导航模块  命名规范：   ...(项目名称，例：xtx)-main-nav。 注意导航其实是超链接 应该用li嵌套a
- 这里的快捷菜单是在版心内部的，而且应该是右浮动，所以版心应该在xtx-shortcut的里面，在ul的外面
- 竖线直接在a标签后面和li标签前面加
- 给ul加右浮动直接加在标签里面加class属性,class="fr", 这个是在base.css中定义的
- 设置选择快捷导航栏的外边距 对a标签设置margin
- 给最后一个手机版去掉margin-right 使用伪类::last-child , 再使用margin-right: 0
- line-height对ul设置li设置a设置都可以 
- 这里手机那个图标我先用iconfont试一下，后面再用精灵图




## 快捷菜单 xtx-shortcut 
-         <!-- 快捷菜单(shortcut)模块 命名规范：  ...(项目名称，例：xtx)-shortcut -->
        <div class="xtx-shortcut">

            <div class="container">
                <ul>
                    <li><a href="#">请先登录</a></li>
                    <li><a href="#">免费注册</a></li>
                    <li><a href="#">我的订单</a></li>
                    <li><a href="#">会员中心</a></li>
                    <li><a href="#">帮助中心</a></li>
                    <li><a href="#">在线客服</a></li>
                    <li><a href="#">
                        <span class="iconfont icon-mobile"></span>
                        手机版
                    </a></li>
                </ul>

            </div>
            
        </div>
        <!-- 快捷菜单(shortcut)模块 命名规范：  ...(项目名称，例：xtx)-shortcut -->






