Zing Gallery
============

基于node.js的web相册，让摄影照片的展示更加简单

### 1、功能

此[Demo](http://120.24.181.238/gallery/)供体验。

* 自动获取照片信息（快门、光圈、ISO、时间等）
* 自由为相册设置信息（封面、名称、描述）
* 相册可加密访问
* 适配PC与移动侧展示
* 移动侧可使用多指手势操控图片，与原生图库一般流畅

### 2、使用

相册基于node & npm，所以这两个工具必不可少。

1. 将照片放入``resources/photos``文件夹
2. 执行命令``npm i``安装依赖
3. 执行命令``npm run start``启动相册

### 3、高级用法

#### 3.1 设置全局信息

编辑``config.js``文件（目前仅有设置标题一项，待填坑…）

#### 3.2 设置相册信息

比如有一个叫xxx的相册，它的位置应该是``resources/photos/xxx``

新建一个info.json文件，位置是``resources/photos/xxx/info.json``

通过这个文件，可以设置相册信息：

```
{
  "description" : "1983年小巷12月晴朗……",     // 该相册的描述；如果没有，则不展示
  "thumbnail" : "IMG_0424.jpg",             // 封面图；如果没有，则默认取第一张作为封面
  "name": "第七章",                          // 相册名；如果没有，则相册名为xxx
  "noDate": false                           // 不展示时间；如果为true，则不展示照片时间信息；默认没有，即false
}
```


### 4、前端开发者

如果你是前端开发者，需要做一些页面上的定制，你需要使用webpack进行开发。

执行命令``npm run dev``（不压缩，一般开发时用）或``npm run dist``（压缩）

将``assets/src``里的源文件编译到``assets/dist``目录。
