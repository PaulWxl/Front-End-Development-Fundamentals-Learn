- 过渡效果
- transition
- 属性名/all + 过渡时间（必须加上秒（s））
- all表示所有能过渡的属性都会产生过渡效果
- 或者单独设置属性，不同属性用英文逗号分开，而且还是得加时间
- transition: width 1s, height 2s; (但是我测试好像不无效，还是按照all来的，根据你那个hover里面变化的)
- 必须给元素本身加
- 一般配合伪类hover使用 :hover
- div {
            width: 200px;
            height: 200px;
            background-color: pink;
            transition: all 3s;
        }
        div:hover {
            width: 400px;
            height: 400px;
            background-color: skyblue;
        }
- 