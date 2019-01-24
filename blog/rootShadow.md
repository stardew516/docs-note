---
title: root-shadow
date: 2018/06/22
tags: javascript
categories: 前端基础
---

## 如何查看控制台隐藏样式shadow-root

1.打开视频：[萌鸡小队](https://m.baidu.com/sf?pd=video_page&sign=2644424138019201916&word=%E8%90%8C%E9%B8%A1%E5%B0%8F%E9%98%9F&title=%E8%90%8C%E9%B8%A1%E5%B0%8F%E9%98%9F%E8%B6%A3%E5%84%BF%E6%AD%8C%2008%20%E4%B8%80%E8%B5%B7%E8%B7%B3%20%E8%90%8C%E9%B8%A1%E5%B0%8F%E9%98%9F%E8%B6%A3%E5%84%BF%E6%AD%8C%3A%E4%B8%80%E8%B5%B7%E8%B7%B3&atn=index&alr=1&openapi=1&resource_id=5052&frsrcid=4185&frsrcid=4185&cambrian_id=1612732424718028&sp=0&lid=7077586335230192403&lid=10376528520655479462&backup_lid=7077586335230192403&ext=%7B%22src%22%3A%22https%3A%5C%2F%5C%2Fvdse.bdstatic.com%5C%2F5ad195742858df836979a139dcbda601.mp4%3Fauthorization%3Dbce-auth-v1%252Ffb297a5cc0fb434c971b8fa103e8dd7b%252F2017-05-11T09%253A02%253A31Z%252F-1%252F%252Ff42897bd8c5ec432eda2bba25e1c1a192c805a481026033111a026e9d1b1f9d0%22%2C%22loc%22%3A%22http%3A%5C%2F%5C%2Fm.v.qq.com%5C%2Fx%5C%2Fpage%5C%2Fh%5C%2Fi%5C%2Fv%5C%2Fh0543ehxviv.html%3Fptag%3D4_5.9.0.21014_copy%26%22%2C%22log_loc%22%3A%22http%3A%5C%2F%5C%2Fm.v.qq.com%5C%2Fx%5C%2Fpage%5C%2Fh%5C%2Fi%5C%2Fv%5C%2Fh0543ehxviv.html%3Fptag%3D4_5.9.0.21014_copy%26%22%2C%22duration%22%3A%22133%22%2C%22poster%22%3A%22http%253A%252F%252Ft11.baidu.com%252Fit%252Fu%253D1009474117%252C1911095290%2526fm%253D171%2526app%253D20%2526f%253DJPEG%253Fw%253D640%2526h%253D362%2526s%253D138AA6EA4E1351C6108146120300D056%22%2C%22source%22%3A%22%5Cu817e%5Cu8baf%5Cu89c6%5Cu9891%22%2C%22s%22%3A%224fc5a291ae508fd21bb2c993d2c599d2%22%2C%22isHttps%22%3A1%2C%22isCompilation%22%3Anull%2C%22jsy%22%3A1%7D&top=%7B%22sfhs%22%3A1%2C%22_hold%22%3A2%7D&fr0=A&fr1=A&referlid=10376528520655479462&ms=1&frorder=2&sfr_fb=0)
---
打开一个视频链接

打开控制台，此时video样式显示如下：
 <!-- more -->
![clipboard.png](http://plq1zlo1f.bkt.clouddn.com/docs-note/blog/root_shadow11.jpg)
2.设置
---
点击右上角竖着的...，选择settings，如上图，显示如下图：
![clipboard.png](http://plq1zlo1f.bkt.clouddn.com/docs-note/blog/root_shadow22.jpg)
找到Elements，勾选 show user agent shadow DOM，再回到控制台，就可以看到隐藏的样式了。如下图所示：
![clipboard.png](http://plq1zlo1f.bkt.clouddn.com/docs-note/blog/root_shadow33.jpg)

##### [转自] [如何查看控制台隐藏样式shadow-root]()