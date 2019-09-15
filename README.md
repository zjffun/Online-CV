# online-resume

示例：https://zjffun.github.io/online-resume/

首先在线简历的好处有很多，我就不一一列举了，直接进主体。

## 设计

先弄清楚最后想要做出来什么东西是个好习惯，整理整理要实现的功能，要显示的内容，整个页面的布局和颜色、整体的架构（做个在线简历这么小的东西就用不上了），用到的框架、库、工具什么的。

### 功能

1. 导出 HTML 和 pdf 功能：这个简历以后会用到其他地方肯定是要导出的。主要要实现导出 pdf 因为别的格式都有弊端（如，图片：无法复制，HTML：hr 可能使用错误地软件打开）。
2. 国际化功能：让世界看到你的简历 —— Online-CV 相信咸鱼的力量！

### 内容

对智联、拉钩、BOSS直聘等招聘网站简历需要填写的内容整理了一下，取其精华得到 以下内容：

- 个人基本信息
- 技能
- 工作经验
- 项目经历
- 教育经历
- 自我描述
- 社交主页
- 作品

### 页面

1. 个人信息和和下面的项目纵向排列：网上有一些是将个人信息放在侧边的设计 ，但这样适合一页的应届生简历，超过一页侧面就很尴尬了。
1. 移动端适配：肯定要在移动端上可以看的
1. 整体背景为浅绿色：这~~就是爱情~~样护眼嘛

### 技术

Webpack、Babel是肯定要用的、之后做成用 YAML 配置内容、打印还会加

## 实现

因为明天要用，所以我准备今天撸出来个初版

1. 首先先完成 HTML ，好的网页应该在没有 CSS 的情况下也能很好的显示：[HTML Complete. · 1010543618/Online-CV@5dd7d9e](https://github.com/1010543618/online-resume/commit/5dd7d9edee7d52d756afdcb226251dc198196571)
2. 然后完成 CSS ，好的网页应该在没有 JS 的情况下也能很好的显示：[CSS complete. · 1010543618/Online-CV@bc494da](https://github.com/1010543618/online-resume/commit/bc494da64a2d6466814557d1bca63ebc445d0327) （现在响应式还不怎么好，不过已经够明天打印的了）
3. 完成响应式，打印的话直接`ctrl + p`就行。i18n 倒是有很多现成的，但感觉不太对劲，继续研究研究。。[i18next](https://www.i18next.com/) 不错，但这么一个页面用配置生成和直接新建一个页面几乎一样啊（新建的页面还更灵活），除非像 Swagger 一样形成个规范（简历有什么规范。。弃坑了）。

