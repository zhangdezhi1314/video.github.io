﻿## 在线体验地址:http://vip.52tech.tech/
## 项目预览
![image](https://github.com/xiugangzhang/vip.github.io/blob/master/static/images/preview.gif)
- 主页面
![image](https://github.com/xiugangzhang/vip.github.io/blob/master/static/images/preview.jpg)
![image](https://github.com/xiugangzhang/vip.github.io/blob/master/static/images/tv.jpg)
- 登录页面
![image](https://github.com/xiugangzhang/vip.github.io/blob/master/static/images/login.jpg)
- 注册页面
![image](https://github.com/xiugangzhang/vip.github.io/blob/master/static/images/register.jpg)
- 会员中心
![image](https://github.com/xiugangzhang/vip.github.io/blob/master/static/images/user.jpg)
- 电影播放页面
![image](https://github.com/xiugangzhang/vip.github.io/blob/master/static/images/play.jpg)
- 电影弹幕功能
![image](https://github.com/xiugangzhang/vip.github.io/blob/master/static/images/danmu.gif)
![image](https://github.com/xiugangzhang/vip.github.io/blob/master/static/images/05.jpg)



## 视频网站项目静态页面目前已经完成的功能：
- 1. 首页导航栏，中部轮播图，以及电影列表的展现，底部导航链接
- 2. 注册页面
- 3. 视频播放页面
- 3. 登录页面
- 4. 用户管理页面

## 视频网站项目动态页面目前已经完成的功能主要功能（dynamic目录）：
 - 1. 用户主页的搭建：
    - 实现了主页轮播图的显示和切换，用户可以从数据库中自由配置和切换轮播图的显示
    - 实现了主页电影列表的显示：从数据库文件读取电影和电视剧列表信息并在前台显示
 - 2. 用户登录和注册页面的搭建：
    - 实现了用户的登录和注册功能
    - 用户注册和登录验证码提示功能
 - 3. 电影播放页面的搭建
    - 对于其他页面的任意可以展现电影列表的页面，用户可以直接点击列表，直接进入播放页面
    - 播放页面电影详细信息的展现
    - 对于加载速度较慢的视频，用户可以自由切换播放接口进行加速
    - 弹幕功能（特色功能）：类似于B站等其他视频网站的弹幕功能，用户在登录之后可以实现在线发言
    - 用户可以在相应的播放页面查看其他用户已经发表的评论，同时也可以在登录之后自由发表评论
    - 电影收藏和取消功能
 - 4. 用户中心的管理
    - 对于已经注册的用户，实现用户基本信息的修改
    - 用户密码的修改
    - 用户评论记录的查看
    - 用户收藏电影的查看和播放
    - 用户登录日志的查看
 - 5. 电影搜索功能（特色功能）
    - 实现了根据视频播放地址和视频名称全网视频的搜索和播放功能
    - 实现了正在热映，即将上映和TOP250的电影列表的展示
  - 5. 其他
    - 页面整体的风格模仿了Discuz等论坛网站的布局
    - 网站首页的轮播图效果模仿了优酷、爱奇艺、腾讯视频等主流视频网站的轮播图效果
    - 电影底部的的友情链接，使用了大部分网站的分栏布局，用户可以添加自己的QQ群以及微信公众号方便增加自己网站的人气
    - 主要列表的分页功能，对于一些内容显示较多的不能再一页显示完整的页面，使用了ajax无刷新分页对数据进行多条展示，提高了用户的体验
    - 目前主流浏览器中也做了相应测试，建议大家使用谷歌或者火狐浏览器，效果可能会更好


## 程序安装方法

 - 1. 确保电脑已经安装了NodeJS环境，运行版本尽量保持最新（V8以上吧），然后下载此安装包后解压到你的系统任意盘符下面的目录；
 - 2. 在当前解压文件夹的主目录，dynamic文件夹（包含package.json的那个文件夹）运行命令：npm install， 系统就会自动安装该程序的依赖包；
 - 3. 在以上的步骤都执行完成且正确的情况下，就可以在程序主目录下面（有app.js的那个目录）,运行命令
 ```
    node app.js
 ```
 之后就会自动在浏览器中打开本程序安装的主界面；
 - 4. 如果是windows环境下，本程序提供了可视化的安装。用户可在程序的安装界面输入数据库名、数据库主机地址、数据库用户名、数据库密码，之后点击按钮立即安装即可，在输入的参数全部正确的情况下，就会后台自动安装程序，安装成功之后会自动跳转到网站首页；
 ![image](https://github.com/xiugangzhang/vip.github.io/blob/master/static/images/install.jpg)
 - 5. 如果是Linux环境下，请在程序的根目录下面（与app.js同级目录）创建一个config.properties文件，并将下面的内容删除注释后，复制到这个配置文件里面即可，请确保这里的配置信息和你的数据库配置信息完全一致；
```
database=video           // 数据库名        
host=localhost           // 这里修改为你的数据库主机IP（如果是本地测试：默认为localhost或127.0.0.1）
user=root                // mysql数据库用户名
password=123456          // mysql数据库密码   
```
 -6. 安装程序成功之后，默认数据库是没有测试数据的，首页可能是没有数据展示的，如果需要查看效果，需要用户手动将本程序提供的test.sql文件导入到数据库即可。用户只需要登录你的网站数据库管理界面（PHPAdmin）,如果是在本地测试的话，就使用Navicat等MYSQL数据库连接工具连接数据库，连接完成之后创建数据库名为video，设置数据库登录名root， 登录密码为123456。
 -7. 此外，在配置完成以上步骤之后，如果发现不能正常使用弹幕功能，请修改views/play.xtpl文件下,找到代码此处位置
 ```
 var e,t=io.connect("http://127.0.0.1");
 ```
 将上面的IP地址和端口号修改为服务器的IP地址和端口号即可。
 - 8. 在线演示站点：http://vip.52tech.tech
 - 9. 对于安装和使用的过程中如果有什么问题和建议，也欢迎交流和提出建议，联系邮箱：tech52admin@126.com


## 静态页主要特点
- 1. 未使用任何第三方框架，均为纯原生的HTML，CSS， js实现（至于这个xframe-min-1.0.js文件是我对于JavaScript封装的一个小型的类似于JQuery的框架，可以参见我的GitHub xframe.js这个开源项目）
- 2. 首页轮播图的实现，轮播图的效果为模仿当前爱奇艺，优酷，腾讯视频的首页风格，实现了预告页面的自动轮播，并且对该部分的效果实现进行了代码封装
- 3. 顶部导航栏的实现：这部分使用的是类似于一般博客的布局方式，实现了导航栏固定于顶部的方式
- 4. 电影播放页面：此处也是类似于当前主流网站的的播放页面，左侧为播放窗口，右侧部分为电影的详细信息
- 5. 底部导航：使用分栏的方式实现了底部的导航，前面的搜歌栏位为链接，后面的一个为网站的微信，QQ等联系方式，实现了鼠标移动自动切换效果的实现
- 6. 用户中心：这部分实现了修改密码，评论，登录，日志管理，收藏电影的功能，用户可以自由切换




