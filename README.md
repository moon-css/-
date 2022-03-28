# h5
**h5**是一个基于javascript语言的移动端用户交互网页项目，用于收集需要的社会信息与数据，传播文化。

## 文件库
- cocos2dX.js
- node.js
- stage.js
- Sound.js


## 入门

### 分类
- [翻页h5](https://note.youdao.com/s/JGdd4Xjp)
- [视频h5]()
- [长图h5]()
- [混合模式h5]()（即包含视频也包含长图）

### 图层处理
- [长图h5图层处理]()
- [非长图h5图层处理](https://note.youdao.com/s/LTaHuo4Z)

### 项目开发流程
项目代码编写之前，需要先对处理好的设计稿进行导出，命令名已经都在`package.json`中配置好了。步骤如下：

对psd文件进行切图导出：

```javascript
  npm run export
```
将导出的图片拼接成精灵图（最大尺寸为2048x2048）：
```javascript
  npm run pack
```
获取图层在页面中的数据信息，包括位置，层级等,并将信息写入`js/config.js`文件中：
```javascript
  npm run export2
```
然后我们就可以在本地编写代码并且运行测试，当整体项目（除接口外）都测试没问题之后，我们对项目进行编译，将`TLayer.js`中的代码压缩，生成`game.min.js`，位于`publish/html5`文件夹中：
```javascript
  npm run compile
```
到此为止，我们本地的操作已经全部结束，之后我们只需要打包cdn文件包然后上传到服务器上即可，cdn文件包中包含有`css,images,js,libs,res`五个文件夹，其中`js`文件夹中除原有的几个文件，我们还需将`publish/html5`文件夹中的`game.min.js`文件放入其中。这项工作我们可以在`publish`中创建一个文件夹，命名为创建日期，如0328，然后将cdn相关文件手动放入此文件夹中，也可以运行下面这段代码，自动将所需文件复制进我们所创建的文件夹中：
```javascript
  node node/update_files.js
```
最后，在服务器上运行并测试项目所有功能，包括接口，没有问题之后这个项目就可以上线了。


