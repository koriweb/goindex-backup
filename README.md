前几天我突然发现自己的 goindex 网页打开是一片空白，然后才知道 donwa 大佬删库了，于是我找了其他的仓库部署了一下网页，今天偶然发现网页打不开是有解决办法的，看到了一篇博文，所以就赶快修改了自己的代码，非常感谢，下面是解决方法，另外博文参考自：
- 解决goindex作者删库，导致goindex打不开的问题 - 天下无鱼  https://shikey.com/2020/04/27/goindex-index-js-repack.html
## 解决方法：
- 【可选】首先到 GitHub Fork一份 Goindex 的代码。
- 登录Cloudflare Worker，打开workers，选中项目修改原代码部分的一行即可。具体操作如下 —— 找到以下代码，一般是在 21行/23行 。

![cf代码修改细节](https://ae01.alicdn.com/kf/U324911b4bfea4f5bbd01d83026575b51d.png)
！图片加载不出来可直接访问：http://dwz.date/awtQ

### 另外我发现 goindex 现在的版本可以看 GD 快捷方式的文件了，这样就可以把别人共享的文件直接创建快捷方式，在自己的网页看，非常 nice 。

PS：以下内容为原始内容。

---

![GoIndex](https://raw.githubusercontent.com/koriweb/goindex-backup/master/themes/logo.png)  
  
GoIndex  
====  
Google Drive Directory Index  
Combining the power of [Cloudflare Workers](https://workers.cloudflare.com/) and [Google Drive](https://www.google.com/drive/) will allow you to index you files on the browser on Cloudflare Workers.    

`index.js` is the content of the Workers script.  

## 演示 Demo  
material: [https://index.gd.workers.dev/](https://index.gd.workers.dev/)  
classic: [https://indexc.gd.workers.dev/](https://indexc.gd.workers.dev/)  

## 部署 Deployment
1.在本地安装`rclone`

1.Install `rclone` software locally


2.按照说明绑定网盘

2.Follow [https://rclone.org/drive/]( https://rclone.org/drive/) bind a drive  


3.执行`rclone config file`命令来找到文件`rclone.conf`的路径

3.Execute the command`rclone config file` to find the file `rclone.conf` path

4.打开`rclone.conf`，找到配置`root_folder_id`和`refresh_token`

4.Open `rclone.conf`,find the configuration `root_folder_id` and `refresh_token`  


5.在 https://github.com/donwa/goindex 中下载index.js文件并填写其中root和refresh_token

5.Download index.js in https://github.com/donwa/goindex and fill in root and refresh_token  


6.将代码部署到[Cloudflare Workers]（https://www.cloudflare.com/）

6.Deploy the code to [Cloudflare Workers](https://www.cloudflare.com/)

## 安装部署 Quick Deployment
1.打开 https://installen.gd.workers.dev/ 

1.Open https://installen.gd.workers.dev/


2.授权认证后，生成部署代码

2.Auth and get the code


3.复制代码到CloudFlare进行部署

3.Deploy the code to [Cloudflare Workers](https://www.cloudflare.com/)  



## 关于 About
Cloudflare Workers允许您编写可在Cloudflare的150多个全球数据中心中运行的JavaScript。

Cloudflare Workers allow you to write JavaScript which runs on all of Cloudflare's 150+ global data centers.  
