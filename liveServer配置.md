# liveServer文件监听配置
`liveServer`通过监听文件的变化，向浏览器发送信息，指示浏览器重新加载，而我们可以通过修改它的`settings`文件配置来调制它的监听范围，避免一些不必要的刷新。

1. 安装好`liveServer`后，我们点击查看，打开命令面板，输入`settings`,点击首选项：

<img width="1193" alt="image" src="https://user-images.githubusercontent.com/70060430/221746408-35a4c288-4c64-44d7-b17b-12c31aa49d4c.png">

<img width="1024" alt="image" src="https://user-images.githubusercontent.com/70060430/221747025-40f683bd-4c3e-417a-a5d9-5843d887a6e0.png">

2. 在搜索栏输入`liveServer`即可得到以下`liveServer`相关的设置属性：

<img width="698" alt="image" src="https://user-images.githubusercontent.com/70060430/221749050-8512134d-f3cf-4b19-b8d1-ea04a631b1bc.png">

3. 找到我们所需要的属性名称（以`ignoreFiles`为例），点击下方的在*settings.json*中编辑，进入示例界面，复制对应的代码粘贴到我们自己文件夹中的*settings.json*(在.vscode文件夹中，如果没有找到对应文件夹，调整自己的电脑状态为隐藏文件夹可见)

<img width="707" alt="image" src="https://user-images.githubusercontent.com/70060430/221747668-2b1290ff-1c06-4195-a277-1e86072bce3c.png">
<img width="518" alt="image" src="https://user-images.githubusercontent.com/70060430/221749165-df3259bd-540d-4e9b-aaf7-a2a7739c64cd.png">


4. 在我们自己的`json`文件中复制好代码之后，根据我们自己的需求，调整属性值，然后重启`go live`就可以了,本次我想设置的是让`liveServer`忽视项目文件夹中json文件夹的变化，所以加上了json文件夹的目录路径：`'**/json/*`:
<img width="581" alt="image" src="https://user-images.githubusercontent.com/70060430/221749212-b5ead819-6e40-4725-8c5b-319e237ec2d2.png">


注意点：`settings`中的目录路径修改需要先回到项目目录下,`**/`即回到本文件的上一级目录，`/*`为选中`/`前目录文件夹下的所有文件或文件夹
