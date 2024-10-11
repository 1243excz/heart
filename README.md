### 准备工作

1. `npm i`，安装依赖。
2. `npm run prepare`，安装husky，在`git commit`时会对文件进行格式化。
3. 设置环境变量（windows平台）。以管理员的方式打开cmd。执行`setx /M ACCESS_KEY_ID 自己的ID`以及`setx /M ACCESS_KEY_SECRET 自己的密钥`。设置完后，重启vscode。环境变量会生效。在操作过程中，遇到任何问题可以联系袁浩东。

### 部署模式

1. dev：代表的是开发模式
2. rel：代表的是预生产模式
3. pro：代表的是正式模式

### 部署前

执行`npm run build`

### 部署到对应的环境

1. 部署到开发环境。执行`npm run upload:dev`
2. 部署到预生产环境。执行`npm run upload:rel`
3. 部署到正式环境。执行`npm run upload:pro`

### 部署后

在非正式环境，已自动插入预览链接和vconsole，以及清除数据的按钮。
部署后，可以从`window.deploy.mode`获取到当前的模式，值为以下三个值：`dev`，`rel`，`pro`。在对接后端接口时，需要用到这个值。

### 关于z-index的设定原则
| 组件 | z-index |
| --- | --- |
| modal | 50 |
| toast | 1000 |
| 清除数据的按钮 | 1000 |
| 预览链接 | 1000 |
| 横屏锁定 | 1010 |
| 版本号 | 1000 |
| 加载中 | 1000 |

### roadmap

- [x] 清理之前的代码 - √
- [x] 横屏锁定 - √
- [x] vConsole - √（非正式环境）
- [x] 预览链接 - √（测试环境和预生产环境）
- [x] 清除数据的按钮 - √（非正式环境）
- [x] 禁止双击放大
- [x] 禁止复制文本
- [x] 禁止双指缩放
- [x] 禁止可点击元素的反馈效果
- [x] 禁止图片的点击，长按反馈
- [x] 禁止可滚动元素下拉或上拉至边界时的浏览器默认行为（ios 16版本以下的不支持）
- [x] 路由管理
- [x] api请求
- [x] toast组件
- [x] modal组件
- [x] store：单例类
- [x] 保存海报：html2canvas
- [x] 背景音乐：howler
- [x] 滚动控制：iscroll，better-scroll，perfect-scrollbar
- [x] 轮播图：slick-carousel，swiper
- [x] 预加载：preload.js
- [x] 动效：spine，lottie，序列帧，apng，gif，css animation，js animation，transition
- [x] 实用脚本。重命名，提取字形，压缩图片
- [x] 移动端的浏览器的click事件默认存在300ms的延迟
- [x] 新增实用工具类，文件都在src\js\utils目录
- [x] 添加测试功能
- [x] 读取excel，保存excel：read-excel-file，json-as-xlsx
- [x] 约定pixi.js 和 three.js 版本。pixi.js：8.0.5；three.js：0.162.0。