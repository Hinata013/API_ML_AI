# API_ML_AI

### product requirements

| 发布日期 | 18/11/25 |
|----|----|
| 名称 | 语音输入笔记本 |
| 文件现状 | 未起头 |
| 文件主人 |啊诗本诗 |
| 领头的设计师 | |
| 领头的开发者 | |
| 领头的测试者| |

### 产品介绍
- 语音笔记本是一款区别与语音输入法的短语音输入和普通电子笔记本的纯文字输入的语音输入笔记本。兼顾长语音输入、文字输入和识别图片文字输入的笔记本APP。致力于为用户打造不费时不费力的输入输出体验。

### 目标

- 帮助用户解放双手和双眼，用语音输入与带有文字的图片记录文字，标签功能快速记录与获取信息。为用户带来更便捷快速的体验，构建一个帮助用户提升技能，快速记录与思考的工具。


### 背景
- 在高速发展的社会下，人们总面对着瞬息万变的信息。为了不与世界脱节，便需要更快地行动与更好的节省时间和精力。而在市场上，若用户想完成从语音-文字的操作，需要一个可语音输入的输入法与一个备忘录来进行重复操作，且大部分语音输入法并无长语音输入功能。且大部分备忘录并无自分类功能，或需要用户手动寻找，或需要用户在使用过程中再增加手动增加分类、拖入分类的过程。稍微麻烦。并且当用户只有一张写满文字的图片时，就需要一个个手动输入。
- 在目前市场上，语音笔记本大致分为两类，一是只储存录音文件，二是只有转文字功能。语音转文字与文字识别集一体的笔记本工具较少

 
### 战略契合处
1. 本产品在编辑时，用户可以直接选择使用长语音输入，由系统在文档中转换成文字进行记录。本功能大幅提升了用户的录入效率，方便后期的文字处理和内容存档，省去记录的人力和时间成本。
2. 用户可以上传一张带有文字的图片，系统在本文档中转换成可编辑的文档文字。
3. 当用户完成一篇文章的编辑后，系统对文章的标题和内容进行深度分析，输出能够反映文章关键信息的主题、话题、实体等多维度标签，方便用户日后寻找。
4. 用户登录后可以将文章上传云端实现同步，也可以实现跨平台分享给其他社交平台上的朋友。

### 情境假设
- 用户需要在手机上联网使用。
- 用户使用语音输入功能时，需要给出麦克风权限。
- 用户使用图片上传功能时，需要给出存储与摄像头功能。

### 用户画像
- 针对有长语音转化文字需求，拍照/上传图片转化文字需求，记录频繁、对文章分类头疼的15-35岁用户，如作家、学生、公司职员等。

###  用户需求
|#| 使用场景 | 问题需求 |重要程度 |对应功能|对应API|
|----|----|----|----|----|----|
|1| 在需要快速记录一大段讲话时，既无法手打快速输入，也无法依赖输入法的短语音输入 | 快速、准确录入长语音 |最重要 |长语音输入| 百度长语音识别|
|2| 当只有一张满是文字的图片时，对慢慢手打感到心累 | 需要一种方法快速获取图片上的文字转化为可编辑的文字 | 重要|图片转文字 | 百度通用文字识别|
|3| 在面对一大堆杂乱无章排列的文章时，无法快速找到自己想要的部分或一篇 |需要用一种方法让文章被快速分类 |次重要|文章标签 | 百度文章标签|

### 产品功能架构
![产品功能架构.jpg](https://upload-images.jianshu.io/upload_images/14325233-aa879b91f77a0d7a.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
[产品功能架构](#产品功能架构.html)

### 流程图
![流程图.jpg](https://upload-images.jianshu.io/upload_images/14325233-a05a43995d330ca1.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
[流程图](#流程图.html)
### 全局说明
1. 功能权限分为登录/未登录两个状态。
（1）登录：登录状态下可进行app内所有操作。
（2）未登录：只能使用编辑文章，文章列表视图设置，标签，分享文章至其他平台功能。不能使用云端，账号功能。
2. 激活编辑界面时自动弹出tab，再次点击编辑界面空白地区时弹出输入法。

### 使用者交互及设计
![使用交互.jpg](https://upload-images.jianshu.io/upload_images/14325233-82c92a0a00f6623a.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
[使用者交互](#index.html)
### 迭代功能
- 上线搜索功能
- 语音朗读功能
