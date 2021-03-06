* ArthurSlog
* SLog-29
* Year·1

* Guangzhou·China
* Aug 3th 2018

![关注微信公众号“ArthurSlog”](https://github.com/BlessedChild/LogofAxu/blob/master/images/icon_128.jpg?raw=true "微信扫描二维码，关注我的公众号")

* [GitHub](https://github.com/BlessedChild/ArthurSlog)

* [掘金主页](https://juejin.im/user/59f2a424f265da432f305c66/posts)

* [简书主页](https://www.jianshu.com/u/b9ebe10f0534)

* [segmentfault](https://segmentfault.com/u/arthurslog/articles)

大学毕业 交了几万块钱的学费 完成了所有学业要求 然后社会就会为你买单吗？ 有的人花了几十万也只是获得月薪几千块的一个职位 而你 花了几万块钱和几个月的时间 就想让社会每月掏个万把块钱来买单啊？ 就这样的智商 先不论培训得会不会 这样的智力水平迟早也得返乡 

---

### 开发环境MacOS(High Sierra 10.13.5)

#### 需要的信息和信息源：

* Slog1_如何使用nodejs与mysql进行数据交互
* Slog4_使用后端框架KOA实现静态web服务器
* Slog6_使用vue前端框架实现单页应用(SPA)
* Slog24
* Slog25
* Slog26

##### 前端部分：

* 统计页面-计算属性和侦听器、https://cn.vuejs.org/v2/guide/computed.html 主页：index.html

* 注册界面-条件渲染、https://cn.vuejs.org/v2/guide/conditional.html :signup.html

* 登陆界面 :signin.html

* 后台用户管理的界面-列表渲染、https://cn.vuejs.org/v2/guide/list.html 用户界面: account.hmtl

* 调查问卷-文本、多行文本、复选框、单选按钮、选择框、https://cn.vuejs.org/v2/guide/forms.html : form.html

* 离开页面提醒-事件处理、https://cn.vuejs.org/v2/guide/events.html 

* 移动端样式兼容-Class与Style绑定、https://cn.vuejs.org/v2/guide/class-and-style.html

##### 后端部分：

* 数据库数据交互模块-部署、配置

* 静态web服务器

* 用户注册模块

* 用户登陆模块

* 统计分析模块

* 用户状态模块-超时、无效、非法

##### 关键思路

### 开始编码

* 切换至 client 文件夹路径下

> cd client

* 创建一个新的文件夹 “js” 用于存放前端的 js 文件

> mkdir js

* 我们现在来更新 signup.html 注册页面的前端样式，在js文件夹里创建一个js文件 signup.js，这个，就是vue框架文件，指导客户端前端的js文件

> cd js

signup.js
``` js
new Vue({
    el: '#signup-container',
    data: {
      sex: ''
    }
  })
```

* 我们在 signup.html 里面引用这个新编写的js文件

signup.html
``` html
<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8">
    <link rel="stylesheet" type="text/css" href="./css/style.css" >
    <title>signup_ArthurSlog</title>
</head>

<body>

    <div class="signup-container">
        <div>This is signup's page by ArthurSlog</div>
        <p>Singup</p>
        <form action="http://127.0.0.1:3000/signup" method="GET">
            Account: <br>
            <input type="text" name="name"> 
            <br>
            Password: <br>
            <input type="text" name="password">
            <br>
            Again Password: <br>
            <input type="text" name="repassword">
            <br>
            First Name: <br>
            <input type="text" name="firstname">
            <br>
            Last Name: <br>
            <input type="text" name="lastname">
            <br>
            Birthday: <br>
            <input type="text" name="birthday">
            <br>

            <br>
            <div>
                <span>Sex: {{ sex }}</span>
                <br>
                <input type="radio" id="one" value="Male" v-model="sex">
                <label for="one">Male</label>
                <br>
                <input type="radio" id="two" value="Female" v-model="sex">
                <label for="two">Female</label>
            </div>
            <br>

            <br>
            Age: <br>
            <input type="text" name="age">
            <br>
            Wechart: <br>
            <input type="text" name="wechart">
            <br>
            QQ: <br>
            <input type="text" name="qq">
            <br>
            Email: <br>
            <input type="text" name="email">
            <br>
            Contury: <br>
            <input type="text" name="contury">
            <br>
            Address: <br>
            <input type="text" name="address">
            <br>
            Phone: <br>
            <input type="text" name="phone">
            <br>
            Websize: <br>
            <input type="text" name="websize">
            <br>
            Github: <br>
            <input type="text" name="github">
            <br>
            Bio: <br>
            <input type="text" name="bio">
            <br><br>
            <input type="submit" value="完成注册">
        </form>
        <a href="./form.html">Signup</a>
        <br>
        <a href="./index.html">Return index's page</a>
        <br><br>
    </div>  

</body>

</html>
```

* 切换至server文件夹路径下

> cd server

* 现在，启动静态web服务器

> node index.js

* 现在打开浏览器，在地址栏输入 127.0.0.1:3000，正常显示主页后，点击 signup 链接，正常情况下，你会看到 sex 选项变成单选按钮了

* 至此，我们使用 vue模版语言 更新了 signup.html 这个注册页面的 sex 选项的样式为单选按钮。

---

### 欢迎关注我的微信公众号 ArthurSlog

![ArthurSlog](https://github.com/BlessedChild/LogofAxu/blob/master/images/icon_128.jpg?raw=true "微信扫描二维码，关注我的公众号")

### 如果你喜欢我的文章 欢迎点赞 留言
### 谢谢
