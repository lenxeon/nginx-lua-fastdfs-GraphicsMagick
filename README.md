nginx-lua-fastdfs-GraphicsMagick

==================
这是从[https://github.com/hpxl/nginx-lua-fastdfs-GraphicsMagick](https://github.com/hpxl/nginx-lua-fastdfs-GraphicsMagick)fork过来的修改版本
相对于原版本，作出了详尽的注释，详情见lua/fastdfs.lua

本版本支持了三种方式的缩略图生成 _(width)x(height)_m[1-3].(file_expand)

原文件 
http://localhost/group1/M00/01/7C/OkTuVFTPLhiAXLOtAADCVxCAPKc352.jpg
http://localhost/group1/M00/01/7C/OkTuVFTPLhiAXLOtAADCVxCAPKc352.jpg_400x0_m1.jpg  定宽缩放模式
http://localhost/group1/M00/01/7C/OkTuVFTPLhiAXLOtAADCVxCAPKc352.jpg_400x400_m2.jpg 等比缩放并裁减多余的，如头像logo等
http://localhost/group1/M00/01/7C/OkTuVFTPLhiAXLOtAADCVxCAPKc352.jpg_400x400_m3.jpg 等比绽放不裁减，会有空白间隙

获取原文件时，本版本直接向fastdfs要的源数据并输出，并没有先写到本地，各位可自行决定
定时清除crontab.sh定时任务凌晨清除7天内未访问的图片，节省空间，需添加到系统任务中


参考网址
----------------
1. [https://github.com/hpxl/nginx-lua-fastdfs-GraphicsMagick](https://github.com/hpxl/nginx-lua-fastdfs-GraphicsMagick)
1. [https://github.com/openresty/lua-nginx-module](https://github.com/openresty/lua-nginx-module)
2. [https://github.com/azurewang/Nginx_Lua-FastDFS](https://github.com/azurewang/Nginx_Lua-FastDFS)
3. [https://github.com/azurewang/lua-resty-fastdfs](https://github.com/azurewang/lua-resty-fastdfs)
4. [http://rhomobi.com/topics/23](http://rhomobi.com/topics/23)
5. [http://bbs.chinaunix.net/thread-4133106-1-1.html](http://bbs.chinaunix.net/thread-4133106-1-1.html)
