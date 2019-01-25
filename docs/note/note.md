# note  

> 获取宽高  

获取页面宽度winW: `parseInt(document.body.clientWidth, 10);`  
获取元素id宽度：`document.getElementById("id").offsetWidth;`  

> 手机边框1px  

```
/* 上 */  
.borderTop:before {content:"";position:absolute;z-index:2;left:0;top:0;height:1px;width:100%;border-top:1px solid #ccc;-webkit-transform-origin:0 0;transform-origin:0 0;-webkit-transform:scaleY(.5);transform:scaleY(.5);}

/* 下 */  
.borderBottom:after {content:"";position:absolute;z-index:2;left:0;bottom:0;height:1px;width:100%;border-bottom:1px solid #ccc;-webkit-transform-origin:0 100%;transform-origin:0 100%;-webkit-transform:scaleY(.5);transform:scaleY(.5);}

/* 左 */  
.borderLeft:before {content:"";position:absolute;z-index:2;left:0;top:0;height:100%;width:1px;border-left:1px solid #ccc;-webkit-transform-origin:0 0;transform-origin:0 0;-webkit-transform:scaleX(.5);transform:scaleX(.5);}

/* 右 */  
.borderRight:after {content:"";position:absolute;z-index:2;right:0;top:0;height:100%;width:1px;border-right:1px solid #ccc;-webkit-transform-origin:100% 0;transform-origin:100% 0;-webkit-transform:scaleX(.5);transform:scaleX(.5);}
```

> 超出边界...ellipsis  

```
.ellipsis-l1{
  max-height: 20px;
  line-height: 20px;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 1;
  -webkit-box-orient: vertical
}
.ellipsis-l2{
  max-height: 40px;
  line-height: 20px;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  /*! autoprefixer: off */
  -webkit-box-orient: vertical;
}
```
> 复选框checked失效  

解决：原生this.checked

> 项目重复启动 bind in use  

解决：jps 查看启动端口  kill 987杀死 kill -9 987强制杀

> mac下重装nginx  

```
1. nginx -s stop 停止nginx进程
2. which nginx 查看nginx所在目录  删除
3. brew remove nginx
4. brew install nginx
```

> 免费的图床  

https://portal.qiniu.com/bucket  
https://tu.aixinxi.net/index.php  
https://sm.ms/  
http://www1.freep.cn/  
http://jiantuku.com/#/ 
https://tu.aixinxi.net/ 
https://pic.xiaojianjian.net/  
https://upload.ouliu.net/  

> 判断是否为数组  

```
1).toString.apply(v) === '[object Array]'
2).return Object.prototype.toString.call(obj) === '[object Array]'
3).arr instanceof Array
4). Array.isArray(arr)
```

> express安装  

```
1. npm install express -gd
2. npm install -gd express-generator
3. express -V
```

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>

>