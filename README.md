使用工具：
Node.js + Browser-Sync

现实情况：

可能很多刚入门的前端小伙伴，都会有这样的经历。改一下，就要各种刷新浏览器，很影响工作效率。

 
原理:node 监控项目文件夹 文件改动就更新页面。

第一步：

安装nodejs

 按 win + r 键，输入cmd 按下Enter，输入命令 node -v

$node -v
可以查看node版本号.确认安装成功。

第二步：安装淘宝镜像，可以安装npm更快。安装完成后，使用 cnpm -g -install [这里是你要下载的包]

$ npm install -g cnpm --registry=https://registry.npm.taobao.org
　　 

第三步：全局安装，Browser-Sync。

$npm install -g browser-sync
　

第四步：使用cmd进入你项目所在的文件夹 [ 千万不要在根目录，会坚持根目录的文件，拖慢电脑速度 ]，输入以下代码：

$browser-sync start --server --files "**"   监控css和html改变


//创建服务器 $browser-sync start --server --files "**" 


//代理服务器 $browser-sync start --proxy "localhost" --files "**" 


可以监控js，css和html改变，Ctrl+s 保存。即可在浏览器实时刷新


 输入 http://localhost:3000 即可访问，访问文件夹下的html加上对应的路径即可。PS：可以多个浏览器输入网址后分别运行，不影响操作。使用代码编辑程序后，

Ctrl+s 保存后，可以实时刷新。
