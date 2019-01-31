# error  

> 页面两个div之间有一个小margin，样式怎么改都去不掉  

解决：html中div换行了，把两个div放到同一行就好了。

> app上点击有背景  

解决：全局添加样式`-webkit-tap-highlight-color: rgba(255, 255, 255, 0);`

> 手机端input边框阴影  

解决：添加`-webkit-appearance: none;`

> chrome模拟器里点击元素错位  

解决：我把百分比改成fit to window 好了
![phone-scale](../assets/scale.jpg ':no-zoom')

> git push 报错`RPC failed; curl 55 SSLWrite() returned error -9805`  

解决：一次性提交代码太多导致，使用git log找到最近一次commit的代码，git reset {id}回退到commit前的状态，再分批次提交。

> 代码丢失，git log找不到  

解决：`git reset --hard xxx`的记录，使用`git reflog`。

> sudo nginx -s reload启动nginx报错：`nginx: [error] open() "/usr/local/var/run/nginx.pid" failed (2: No such file or directory) ` 

解决：`sudo nginx -c /usr/local/etc/nginx/nginx.conf => sudo nginx -s reload`

> input中type为number时maxlength失效  

解决：`input type="tel"`

> 微信授权callback有多个参数，出现丢失的情况。  

解决：因为授权接口中&的多个参数会变成整个接口地址的参数，所以需要对&进行加密，使用`var callbackurl = encodeURIComponent(window.location.href)`进行加密

> 滚动不顺畅  

解决：添加样式
```
-webkit-overflow-scrolling: touch;
-webkit-font-smoothing: antialiased;
-moz-osx-font-smoothing: grayscale;
```

> 事件冒泡  

解决： stopPropagation,cancelBubble(ie)

> 移入移出多次触发  

解决： mouseleave 对子元素不生效，不会冒泡

> 安装navicat，完成后提示文件损坏  

解决： 打开终端，输入`sudo spctl --master-disable`

> docsify配置的搜索功能失效  

解决：回到文档首页（文档根目录），打开控制面板，找到localstorage，删除docsify.search.index和docsify.search.expires，刷新页面。


> textarea里输入的换行、空格直接存到所需样式的div里时，没效果。  

解决：转义一下，空格替换成`&nbsp;`换行\r\n换为`<br>`，template里使用{{{}}}而非{{}}解析。
```
nl2br: function (str, idx, tag, isXhtml) {
  let blankTag = '&nbsp;'
  let breakTag = (isXhtml || typeof isXhtml === 'undefined') ? '<br />' : '<br>'
  let newStr = (str + '').replace(/([^>\s]?)(\s)/g, '$1' + blankTag + '$2')
  newStr = (newStr + '').replace(/([^>\r\n]?)(\r\n|\n\r|\r|\n)/g, '$1' + breakTag + '$2')
  if (tag) {
    this.changeData[idx][tag] = newStr
  }
  return newStr
}
```
**还可直接添加样式`white-space: pre-wrap;`** 

> html2canvas画出来的图片模糊  

解决：只要这个html整体放大一倍，图片再缩小一倍就可以解决了

> html2canvas把html页面存成图片时，图片不全

解决：先记录当前scrollTop值，window.scrollTo(0,0)到顶部，然后画图，就可以解决了，完了再回到原来的scroll位置 。

> git拉取代码报错：Permission denied (publickey)

解决：
```
j .ssh
git config --global user.name "stardew"
git config --global user.email "hdpu_weilu_0791@163.com"
ssh-keygen -t rsa -C "hdpu_weilu_0791@163.com"
```
拷贝：id_rsa.pub  
放到 https://git.oschina.net/keys 的ssh里  

> 点击事件失效  

解决：使用css `pointer-events: none;`直接穿透当前div

> 类似微信，左滑动出现当前li的一些操作mask，touchmove在手机上失效  

解决：在touchmove里使用一个阈值，`Math.abs(endY-startY)` 是否大于10，来决定是否preventDefault。

> webpack 打包时， No ESLint configuration found  

解决：项目中缺少.eslintrc.js文件，手动在根目录添加上。

> 七牛图片上传，下载文件名改名称

解决：普通的a标签下载，只需要在后面加上download=“1223”。七牛上是在href链接后面添加“？download/name”

> new Vue时报错error  Do not use 'new' for side effects  

解决：报错内容上方添加 /* eslint-disable no-new */

> h5获取地理位置信息时，用户第一次拒绝，后面一直都弹窗用户拒绝信息。  

解决：android，设置-》应用程序管理器-》互联网（自带或安装的其他浏览器）-》权限-》位置信息（重启此开关）

> 新建js代码经常报错import declarations not support by current javascript version  

解决：webstorm =》perference =》languages & frameworks =》javascript =》右侧选择ecmascript6

> android微信里播放video，播放完了以后，关闭之后，video一直处在最顶层，z-index失效。

解决： 网上很多地方都没有找到答案，官网上说是无解的，走了个小弯路。关闭video时，把当前video存一下，然后找到父级，删除video再给父级innerHTML video  问题大致解决，目前只想到了这么个方法。
```
let thisNode = this
let parentNode = thisNode.parentNode
parentNode.removeChild(this)
parentNode.innerHTML = thisNode.outerHTML
```

>  chrome浏览器调试的时候，chrome://inspect连接手机之后，一片空白  

解决：因为chrome调试之初需要连chrome服务器，所以存在翻墙问题，翻墙后就可以查看dom了

> mysql连接报错：ERROR 1045 (28000): Access denied for user 'root'@'localhost' (using password: YES)   

解决：系统偏好设置-》最下面mysql-》进入-》点击initialize database-》输入密码，连解时也输入这个密码。


> mysql连接池错误：`Client does not support authentication protocol requested by server; consider upgrading MySQL client`  

解决：navicat 新建查询输入：`ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '你的密码'`

> 

>

>

>

>