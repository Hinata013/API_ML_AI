### product requirements

| 发布日期 | 18/11/25 |
|----|----|
| 史诗名称 | 语音输入笔记本 |
| 文件现状 | 未起头 |
| 文件主人 |啊诗本诗 |
| 领头的设计师 | |
| 领头的开发者 | |
| 领头的测试者| |

### 目录
- [产品介绍](#产品介绍)
- [目标](#目标)
- [背景](#背景)
- [战略契合处](#战略契合处)
- [情景假设](#情景假设)
- [用户画像](#用户画像)
- [用户需求](#用户需求)
- [产品功能架构](#产品功能架构)
- [流程图](#流程图)
- [全局说明](#全局说明)
- [交互设计](#交互设计)
- [API可行性分析](#API可行性分析)

#### 目录2
- [加值宣言](#战略契合处)
- [核心价值宣言](#战略契合处)
- [用户痛点宣言](#用户需求)
- [AI概率性考量](#API可行性分析)
- [需求列表](#用户需求)
- [交互及界面设计](#交互设计)
- [信息设计](#产品功能架构)
- [使用水平](#API可行性分析)





### 产品介绍
- 语音笔记本是一款兼顾长语音输入、文字输入语音朗读、识别图片文字输入与文章自动分类的笔记本APP。在方便用户快速输入输出的同时加上待办事项提醒、密码锁、悬浮记事、推荐文章等功能，致力于为用户打造不费时不费力的使用体验。

### 目标

- 帮助用户解放双手和双眼，用语音输入与带有文字的图片记录文字，标签功能快速记录与获取信息。为用户带来更便捷快速的体验，构建一个帮助用户提升技能，快速记录与思考的工具。


### 背景
- 在高速发展的社会下，人们总面对着瞬息万变的信息。为了不与世界脱节，便需要更快地行动与更好的节省时间和精力。但单靠文字输入输出已经无法满足用户的多样化需求。

 
### 战略契合处
加值宣言：使用百度长语音输入API、百度通用文字识别API、百度文章标签API为本产品核心功能语音输入、图片识别、文章标签加值。
最小可用产品：可进行语音输入、图片识别的语音笔记本。

1. 本产品在编辑时，用户可以直接选择使用长语音输入，由系统在文档中转换成文字进行记录，大幅提升了用户的录入效率，方便后期的文字处理和内容存档，省去记录的人力和时间成本。
2. 用户上传或现拍一张带有文字的图片，由系统识别后在文档中转换成可编辑的文档文字。
3. 当用户完成一篇文章的编辑后，系统对文章的标题和内容进行深度分析，输出能够反映文章关键信息的主题、话题、实体等多维度标签，方便用户日后寻找。
4. 用户登录后可以将文章上传云端实现同步，也可以实现跨平台分享给其他社交平台上的朋友。
5. 待办事项的提醒可以在忙碌的日子里提醒用户不要忘记重要的事项
6. 密码锁帮助用户锁住所有的私密文档
7. 悬浮在手机其他界面的语音输入小按钮，可以帮助用户随时随地记录
8. 每日根据用户常用标签推荐的业内新闻与其他类型文章可以帮助用户更便捷地获取感兴趣的内容

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
|4| 忙手忙脚时总是忘了接下来要干什么，没有明确规划或总是忘记时间 |需要一个能提醒自己待办事项的功能 |次重要|待办事项提醒 | 无|
|5| 文档中写着自己的私密笔记，不愿被人轻易看到 |需要一个密码锁来帮助封锁 |次重要|密码锁| 无|
|6| 当在手机其他页面忙碌时，赶不及重新点开笔记本进行记录 |需要用一种方法能随时快速进入语音输入界面 |次重要|悬浮记事窗口 | 无|
|7| 想要快速获取自己兴趣所向的文章 |需要用一种方法快速获取资讯 |次重要|美文推荐| 无|


<!-- ### 人工智能概率性
/1. 百度官方宣布百度语音开放平台自 2013 年 10 月上线以来每日在线语音识别请求已经达到了 1.4 亿次，开发者数量超过 14 /万。在如此庞大的数据支撑下，百度语音在“安静条件下”的识别准确率达到了 97%。 /[新闻网址](https://blog.csdn.net/snow2know/article/details/53858131) -->


### 产品功能架构
 [流程图&功能构架&交互原型](https://sssakuraiii.github.io/API_ML_AI/. )
![产品功能架构.jpg](https://upload-images.jianshu.io/upload_images/14325233-2fbcaa25c2d706bb.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 流程图
 [流程图&功能构架&交互原型](https://sssakuraiii.github.io/API_ML_AI/. )
![流程图.jpg](https://upload-images.jianshu.io/upload_images/14325233-32aa30edc7c7f097.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


### 全局说明
1. 功能权限分为登录/未登录两个状态。

&emsp;（1）登录：登录状态下可进行app内所有操作。

&emsp;（2）未登录：只能使用编辑文章，文章列表视图设置，标签，分享文章至其他平台功能。不能使用云端，账号功能。
 2. 激活编辑界面时自动弹出tab，再次点击编辑界面空白地区时弹出输入法。

### 使用者交互及设计
[流程图&功能构架&交互原型](https://sssakuraiii.github.io/API_ML_AI/. )
![交互.jpg](https://upload-images.jianshu.io/upload_images/14325233-2e7eeecef0c34c2d.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### API可行性分析

#### 1. 调用百度API展示
(1). 语音识别输入调用
成功示例：
![语音识别.JPG](https://upload-images.jianshu.io/upload_images/14325233-65f08e859b3e66a0.JPG?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

失败示例：
![语音识别失败.JPG](https://upload-images.jianshu.io/upload_images/14325233-66bf01223612069f.JPG?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

总结：百度语音api在完整吐字时能成功辨别，但在说话人口齿不清，语速过快时无法准确辨别


(2). 图片识别api输入调用
成功示例：
![图片识别成功.JPG](https://upload-images.jianshu.io/upload_images/14325233-0adf595202fea8de.JPG?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

失败示例：

![图片识别.JPG](https://upload-images.jianshu.io/upload_images/14325233-b524cc07992231b6.JPG?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![图片识别失败2.JPG](https://upload-images.jianshu.io/upload_images/14325233-eab9787da8fc7768.JPG?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![图片识别失败3.JPG](https://upload-images.jianshu.io/upload_images/14325233-f1aca09c3e2bc726.JPG?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


总结：可以准确识别出电子印刷体，但会被图片像素影响。对手写体辨别能力较差。拍摄角度，像素，尺寸大小皆会影响到识别效果。

(3). 文章标签api调用
示例：
![标签.JPG](https://upload-images.jianshu.io/upload_images/14325233-c92634a6c2e38180.JPG?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


总结：在获取标签上能力较弱，从文章中获取得到的重点标签词精确度有些不准。

#### 2. 调用百度API代码展示
##### (1).语音识别
调用展示
```
from aip import AipSpeech
import time

APP_ID = '	15239717'
API_KEY = '6ygjUeZcltE9tEUE2LAaXPhR'
SECRET_KEY = 'QTONDHe0lwZPpQGZCcujOG0qeTcZl7Zs'

client = AipSpeech(APP_ID, API_KEY, SECRET_KEY)

def get_file_content(filePath):
    with open(filePath, 'rb') as fp:
        return fp.read()
start_time = time.time()
ret = client.asr(get_file_content('./aideo_files/A2_58.wav'), 'pcm', 16000, {
    'dev_pid': 1537,
})
used_time = time.time() - start_time

print( "used time: {}s".format( round( time.time() - start_time, 2 ) ) )
print('ret:{}'.format(ret))

```
调用结果
```
used time: 8.18s
ret:{'corpus_no': '6592465378279780417', 'err_msg': 'success.', 'err_no': 0, 'result':
['床前明月光，疑是地上霜。举头思明月，低头思故乡。'], 'sn': '148955205071534927957'}
```
#### (2). 语音合成
调用示例
```
from aip import AipSpeech 

import os   
APP_ID = '	15239717'
API_KEY = '6ygjUeZcltE9tEUE2LAaXPhR'
SECRET_KEY = 'QTONDHe0lwZPpQGZCcujOG0qeTcZl7Zs'

client = AipSpeech(APP_ID, API_KEY, SECRET_KEY)
#AipSpeech.setConnectionTimeoutInMillis(10)#超时
a = input('传说有个魔仙堡')

result  = client.synthesis(a, 'zh', 1, {
    'vol': 5,
    'per': 0,
    'spd': 5,
})

if not isinstance(result, dict):
    with open('auido.mp3', 'wb') as f:
        f.write(result)

os.system("auido.mp3")
```
#### (3). 文章标签
调用示例
```
from aip import AipNlp

APP_ID = '15239717'
API_KEY = '6ygjUeZcltE9tEUE2LAaXPhR'
SECRET_KEY = 'QTONDHe0lwZPpQGZCcujOG0qeTcZl7Zs'

title = "虹云工程首星成功发射 打造中国天基互联网"

content = "据微信公众号“中国航天科技集团”（ID： cascwx）12月22日消息，12月22日7时51分，随着一声巨响传来，长征十一号运载火箭在酒泉卫星发射中心一飞冲天，成功将“虹云工程”首星送入预定轨道。长十一火箭由中国航天科技集团有限公司一院抓总研制，是我国长征系列火箭家族第一型固体运载火箭，也是目前我国新一代运载火箭中唯一一型固体型号，使用灵活，可实现多发连续高密度发射。

自2015年9月首飞至今，长十一火箭已连续五次取得圆满成功，体现了高性能和高可靠性。本次发射是该型火箭首次执行1000公里以上太阳同步轨道发射任务。

本次任务的履约周期只有短短半年时间，市场响应能力大大增强，任务适应性大大提高。这得益于长十一火箭型号队伍实施的飞控软件去任务化、并行化集成设计星箭接口和卫星支架等措施。

此外，研制单位创新采用项目承包制等管理模式，7个人只需不到一个月就能完成一发火箭的总装，10天就能完成出厂测试，总装测试效率也大大提高。

“虹云工程”首星是我国发射的首颗低轨宽带通信技术试验卫星，由中国航天科工集团有限公司抓总研制。

本次发射是我国长征系列运载火箭的第295次飞行，也是本年度长征系列运载火箭的第35次发射。


我国低轨宽带通信卫星系统建设实现零的突破

据微信公众号“航天科工空间工程发展有限公司”（iD：casicspace）介绍，虹云工程首星（虹云·武汉号）是我国首颗低轨宽带通信技术验证卫星，同时是首次将毫米波相控阵技术应用于低轨宽带的通信卫星，能够利用动态波束实现更加灵活的业务模式。后续将以此卫星为基础开展低轨天基互联网试验与应用示范。

除通信主载荷外，虹云工程首星还承载了光谱测温仪和3S（AIS/ADS-B/DCS）载荷，实现高层大气温度探测和船舶自动识别系统（AIS）信息、飞机广播式自动相关监视（ADS-B）信息和传感器数据信息采集（DCS），可广泛应用于科学研究、环境、海事、空管等领域。

虹云工程是中国航天科工大力推动的“五云一车”项目之一，由航天科工二院抓总，虹云工程旨在构建覆盖全球的低轨宽带通信卫星系统，以天基互联网接入能力为基础，融合低轨导航增强、多样化遥感，实现通、导、遥的信息一体化。

虹云工程分为技术验证系统、业务试验系统和业务系统三个阶段实施建设：

2018年发射首星，完成技术验证系统建设

十三五末完成业务试验系统建设

预计到十四五具备全面运营条件，实现全球连续无缝覆盖的宽带互联网接入

"

client.keyword(title, content);
```
调用结果
```
{
    "log_id": 4457308639853058292,
    "items": [
        {
            "score": 0.997762,
            "tag": "通信卫星"
        },
        {
            "score": 0.861775,
            "tag": "航空航天"
        },
        {
            "score": 0.845657,
            "tag": "通信"
        },
        {
            "score": 0.83649,
            "tag": "火箭"
        },
        {
            "score": 0.797243,
            "tag": "中国军情"
        }
    ]
}
```



### 迭代功能
- 搜索功能

### 附件
  [流程图&功能构架&交互原型](https://sssakuraiii.github.io/API_ML_AI/. )
