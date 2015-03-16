flex头像编辑上传程序，读取本地图片或使用摄像头拍摄照片，可以截取任意大小。

很实用的一个小功能，例如让用户上传头像，可以使用摄像头拍照或者上传本地的照片，进行裁剪以后上传。这样就遇到了一个麻烦，本来需要一个正方形比例的头像，用户裁了一个长方形比例的照片上传，网站上显示就变形了。所以我在程序中加了可配置项限制长宽比。

在http://code.google.com/p/photo-upload/ 项目基础上进行改进：
自己写了JAVA servlet服务端代码接收flex剪裁好以后的图片上传。
flex端增加了几个可配置参数：要截取的图片的宽和高（图片只能在这个长宽比例内缩放，给用户使用总得限制一个长宽比吧，胡乱裁一个比例上来在你网站上图片显示就不美观了）。服务器端图片存储路径（例如指定存储在/upload/下）。

源代码包含：服务器端（eclipse）和客户端（Flash builder 4/flex builder3）