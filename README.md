# API_ML_AI/期末

|   Title  |   Content  |
| --- | --- |
|  Date(发布日期)  |  2019/12  |
|   Epic(史诗名称) |   学富五车  |
|    Document status(文档状态) |  进行中   |
|  Document owner(文件主人)  |  莫熙彤  |
|  Designer(领头的设计师)  |  莫熙彤  |
|  Developer(领头的开发者)  |   莫熙彤  |
|  QA(领头的测试者)  |  莫熙彤  |

## 产品文档目录
[PRD价值主张设计](#PRD价值主张设计)
- [PRD1.加值宣言](#PRD1加值宣言)
- [PRD2.核心价值](#PRD2核心价值)
- [PRD3.核心价值与用户痛点](#PRD3核心价值与用户痛点)
- [PRD4.人工智能概率性与用户痛点](#PRD4人工智能概率性与用户痛点)
- [PRD5.需求列表与人工智能API加值](#PRD5需求列表与人工智能API加值)

[原型20%](#原型20%)
- [原型1.交互及界面设计](#原型1交互及界面设计)
- [原型2.信息设计](#原型2信息设计)
- [原型3.原型文档](#原型3原型文档)
- [原型4.口头操作说明](#原型4口头操作说明)

[API 产品使用关键AI或机器学习之API的输出入展示 15%](#API产品使用关键AI或机器学习之API的输出入展示)
- [API1.使用水平](#API1使用水平)
- [API2.使用比较分析](#API2使用比较分析)
- [API3.使用后风险报告](#API3使用后风险报告)
- [API4.加分项](#API4加分项)

## PRD价值主张设计15%

### PRD1加值宣言

* 一句话版本：
让用户了解汽车，记录汽车，爱护汽车。

* 一分钟版本：
许多用户对于各种车辆的了解不太熟悉，可能只知道汽车品牌，而不了解每个系列的特色或价格差异，而我们团队设想的这个软件功能是利用车型识别api令用户随时随地在路边看到感兴趣的车，只需要拍照上传到该软件，系统就会进行搜索并列出详细信息；还可以利用车辆外观识别API，用户在汽车受损时可以第一时间拍照上传，识别车辆外观的受损部件和损失类型；该软件还将利用汽车场景文字识别api，提供汽车证件文字识别的功能，方便用户保存关于自己汽车的相关资料，有需要处理相关事务时能够随时查看。

* 目标用户：汽车新手、对汽车感兴趣的人、准备买车的用户、拥有汽车的人

### PRD2核心价值
1.能根据用户拍摄的汽车照片识别出该车的具体车型，输出图片中主体车辆的品牌、型号、年份、颜色、百科词条信息

2.能根据用户拍摄的车辆损伤部位识别车辆外观受损部件及损伤类型，可识别数十种车辆部件、五大类外观损伤（刮擦、凹陷、开裂、褶皱、穿孔）

3.能保存、识别、上传用户所上传的汽车证件

### PRD3核心价值与用户痛点
1.在路边看到心仪的车型却不了解该车的具体属性

2.车辆发生事故不能第一时间了解到具体的损伤情况

2.汽车证件多，找不到相应的软件去储存和归纳

### PRD4人工智能概率性与用户痛点

* 车型识别API（百度智能云）

此款API虽然可识别三千款常见车型，但只是以小汽车为主，大型汽车比如巴士、拖拉机等的车型可能无法识别出准确信息；另外，该API的准确率为90%及以上，对比其他类型的API（如图像识别、文字识别等API，其精确度可达98%及以上），准确度较低，可能会因为过曝或过暗的光照环境影响识别效果，从而降低了用户的使用体验。

* 车辆外观识别API（百度智能云）

此款API与车型识别API一样，只针对常见小汽车车型，大型汽车比如巴士、拖拉机等的车型可能无法识别出准确信息；另外，此款API所需要的识别时长较短，经过测试大概时间为2-4秒，当用户使用时可能会产生不耐烦等情绪。

* 汽车场景文字识别API（百度智能云）

此款API的准确率高，关键字段识别准确率高达99%。但证件毕竟是纸质产品，如果遇到破损或字迹不清的情况则可能会出现无法识别、或者识别出错的情况，因此我们将在产品原型中添加一个手动输入的渠道供客户选择或者对识别错误的结果进行修改。

### PRD5需求列表与人工智能API加值
#### 需求列表

|   用户需求  |   对应标题  |  重要程度  |
| ----- | ----- | ----- |
|   通过拍照识别出车型信息 |   查找车型  |  重要  |
|   通过拍照查看车辆的受损情况 |  查看损伤   |  重要  |
|   通过拍照上传并保存自己的车辆证照信息  |  上传证件  |  次重要  |

#### 人工智能API加值
- 百度智能云 车型识别API [参考来源](https://ai.baidu.com/tech/vehicle/car)

价值宣言：识别车辆的具体车型，以小汽车为主，输出图片中主体车辆的品牌、型号、年份、颜色、百科词条信息；可识别三千款常见车型，准确率90%以上。

此款API能够根据拍摄照片，快速识别图片中车辆的品牌型号，满足用户及时性获取汽车知识的需求；在产品发招的后期，我们团队还将与别的机构合作，提供针对性的信息或服务，可用于相册管理、图片分类打标签、电子汽车说明书、一键拍照租车等场景。

- 百度智能云 车辆外观损伤识别API [参考来源](https://ai.baidu.com/tech/vehicle/damage)

价值宣言：针对常见小汽车车型，识别车辆外观受损部件及损伤类型，可识别数十种车辆部件、五大类外观损伤（刮擦、凹陷、开裂、褶皱、穿孔）

车主或保险公司定损人员通过手机拍摄上传车辆损伤部位的外观图片，系统自动识别受损部件及损伤类型，快速在线定损，并可推荐引导至周边4S店/汽修店，显著提升小额案件的定损、理赔效率。

- 百度智能云 汽车场景文字识别API [参考来源](https://ai.baidu.com/tech/ocr_cars)

价值宣言：基于业界领先的深度学习技术，提供对汽车购买及使用过程中所涉及的各类卡证、票据进行结构化识别的服务

方便客户保存关于自己汽车以及证件的相关资料，有需要处理相关事务却没带证件时能够随时查看。依托百度优秀的深度学习算法和海量优质数据，支持对各角度图片进行识别，并针对特殊情况进行专项优化，关键字段识别准确率高达99%

## 原型 20%
### 原型1交互及界面设计

- 1.拍拍看（自动识别相应API）

![拍拍看](https://gitee.com/NFUNM066/first/raw/master/%E6%8B%8D%E6%8B%8D%E7%9C%8B.jpg)

1.拍拍看可以自动识别所拍摄的具体内容，点击“按下拍照”按钮可查看具体内容的情况。

2.点击“从相册中选择”可以跳转到用户手机里面的相册

3.底部菜单栏图标均可实现点击跳转至相应页面的效果

- 2.拍摄成功（车型识别API）

![拍摄成功（车型识别）](https://gitee.com/NFUNM066/first/raw/master/%E6%8B%8D%E6%91%84%E6%88%90%E5%8A%9F-%E8%BD%A6%E5%9E%8B%E8%AF%86%E5%88%AB.jpg)

1.点击上方“返回重新拍摄可返回到”拍拍看“页面

2.底部菜单栏图标均可实现点击跳转至相应页面的效果。

- 3.拍摄成功（车辆证件文字API）

![拍摄成功（车辆证件文字）](https://gitee.com/NFUNM066/API_Final/raw/master/%E4%BA%A4%E4%BA%922.png)
![跳转证件资料](https://gitee.com/NFUNM066/API_Final/raw/master/%E4%BF%A1%E6%81%AF1.png)

1.点击上方“返回重新拍摄可返回到”拍拍看“页面

2.点击“保存到证件资料”将跳转到“证件资料”页面

3.底部菜单栏图标均可实现点击跳转至相应的页面的效果

- 4.拍摄成功（车辆损伤识别API）

![拍摄成功（车辆损伤识别）](https://gitee.com/NFUNM066/API_Final/raw/master/%E4%BA%A4%E4%BA%923.png)

1.点击上方“返回重新拍摄可返回到”拍拍看“页面

2.底部菜单栏图标均可实现点击跳转至相应页面的效果

- 5.拍摄失败

![拍摄失败](https://gitee.com/NFUNM066/API_Final/raw/master/%E4%BA%A4%E4%BA%924.png)

1.点击“重新拍摄可返回到”拍拍看“页面

2.点击“回到首页”将跳转到首页

3.底部菜单栏图标均可实现点击跳转至相应页面的效果

- 6.证件资料

![证件资料](https://gitee.com/NFUNM066/API_Final/raw/master/%E4%BF%A1%E6%81%AF1.png)

1.系统自动将证件类型划分为目前可以识别的分类

2.点击可进入相对应的分类

3.如果因证件破损而导致拍摄无法识别，可以点击“手动输入”进入手动页面自己进行证件的输入

4.底部菜单栏图标均可实现点击跳转至相应页面的效果

- 7.手动输入

![证件资料](https://gitee.com/NFUNM066/API_Final/raw/master/%E4%BF%A1%E6%81%AF2.png)

1.如果因证件破损而导致拍摄无法识别，可以点击“手动输入”进入手动页面自己进行证件的输入

2.底部菜单栏图标均可实现点击跳转至相应页面的效果。

### 原型2信息设计
#### 产品架构图

![产品架构图](https://gitee.com/NFUNM066/first/raw/master/%E4%BF%A1%E6%81%AF%E6%9E%B6%E6%9E%84.png)

### 原型3原型文档
- [“学富五车APP”原型文档](http://nfunm066.gitee.io/api_final/#id=aku084&p=%E4%BA%A7%E5%93%81%E6%9E%B6%E6%9E%84&g=1)

- [“学富五车APP”原型文档下载](https://gitee.com/NFUNM066/API_Final)

### 原型4口头操作说明

- 该内容已在课堂完成评分

## API产品使用关键AI或机器学习之API的输出入展示
### API1使用水平

1.识别车型，查看汽车详细信息

- 输入：汽车照片（百度智能云 车型识别API）

```

Params
image="图片的Base64编码"
Post
https://aip.baidubce.com/rest/2.0/image-classify/v2/car?access_token="您的access_token"
Header
header: Content-Type: "application/x-www-form-urlencoded"

```
图片如下：

![车辆损伤识别](https://gitee.com/NFUNM066/first/raw/master/%E8%BD%A6%E5%9E%8B%E8%AF%86%E5%88%AB.jpg)

- 输出：汽车的详细信息

```

{
	"log_id": "6767085283381821638",
	"location_result": {
		"width": 1089.7353515625,
		"top": 259.22561645508,
		"height": 524.53283691406,
		"left": 355.47521972656
	},
	"result": [
		{
			"score": 0.97318780422211,
			"name": "丰田兰德酷路泽",
			"year": "2016-2017"
		},
		{
			"score": 0.026246162131429,
			"name": "丰田陆地巡洋舰(LandCruiser)",
			"year": "2016"
		},
		{
			"score": 0.000087816471932456,
			"name": "丰田FJ酷路泽",
			"year": "2017"
		},
		{
			"score": 0.000087267348135356,
			"name": "北汽制造越铃",
			"year": "2014-2017"
		},
		{
			"score": 0.000065810665546451,
			"name": "中兴旗舰(A9)",
			"year": "2017"
		}
	],
	"color_result": "白色"
}

```

2.识别出车辆的具体受损情况（百度智能云 车辆外观损伤识别API）

- 输入：汽车的受损部位照片

```

　　client_id =[百度云应用的AK]
　　client_secret =[百度云应用的SK]
　　#获取token
　　def get_token():
　　host = 'https://aip.baidubce.com/oauth/2.0/token?grant_type=client_credentials&client_id=' + client_id + '&client_secret=' + client_secret
　　request = urllib.request.Request(host)
　　request.add_header('Content-Type', 'application/json; charset=UTF-8')
　　response = urllib.request.urlopen(request)
　　token_content = response.read()
　　if token_content:
　　token_info = json.loads(token_content.decode("utf-8"))
　　token_key = token_info['access_token']
　　return token_key

```

图片如下：

![车辆损伤识别](https://gitee.com/NFUNM066/first/raw/master/%E8%BD%A6%E8%BE%86%E5%A4%96%E8%A7%82%E6%8D%9F%E4%BC%A4.png)

- 输出：车辆的受损部件和损伤类型

```

　　{'log_id': 933845597687207145,
　　result': {'damage_info': [{'numeric_info': [{'area': 10.720499992371,
　　'height': 6.8699998855591,
　　'ratio': 0.12322413921356,
　　'width': 2.0899999141693}],
　　'parts': '前保险杠',
　　'probability': 85,
　　'type': '刮擦'},
　　{'numeric_info': [{'area': 20.604499816895,
　　'height': 10.170000076294,
　　'ratio': 0.72043704986572,
　　'width': 3.0099999904633}],
　　'parts': '左前叶子板',
　　'probability': 65,
　　'type': '凹陷'}]}}

```

3.识别有关汽车证件各种信息（下面以驾驶证为例）（百度智能云 汽车场景文字识别API）

- 输入：驾驶证照片

```

Params
image="图片的Base64编码"
Post
https://aip.baidubce.com/rest/2.0/ocr/v1/driving_license?access_token="您的access_token"
Header
header: Content-Type: "application/x-www-form-urlencoded"

```

图片如下：

![车辆损伤识别](https://gitee.com/NFUNM066/first/raw/master/%E9%A9%BE%E9%A9%B6%E8%AF%81.jpg)

- 输出：驾驶证的信息

```

{
	"log_id": "4162219103781881798",
	"words_result_num": 10,
	"words_result": {
		"证号": {
			"words": "210282198809294228"
		},
		"有效期限": {
			"words": "20150518"
		},
		"准驾车型": {
			"words": "C1"
		},
		"住址": {
			"words": "辽宁省大连市甘井子区"
		},
		"至": {
			"words": "20210518"
		},
		"姓名": {
			"words": "王桃桃"
		},
		"国籍": {
			"words": "中国"
		},
		"出生日期": {
			"words": "19880929"
		},
		"性别": {
			"words": "女"
		},
		"初次领证日期": {
			"words": "20150518"
		}
	}
}

```

### API2使用比较分析
#### 1.图像识别技术
目前我只找到两家公司具有车型识别的技术，如下所示：

- [百度智能云-图像识别技术-车辆分析服务](https://ai.baidu.com/ai-doc/VEHICLE/hk3hb3e3q)
- [腾讯云-图像识别技术-车型识别](https://cloud.tencent.com/document/api/865/36456)

|   对比项  |   百度智能云  |  腾讯云  |
| ----- | ----- | ----- |
|   成熟度 |   文档清晰且详细，旗下的API比较细分，能满足多方面的需要   |   文档较为完善，但涉及到的功能过少 |
|   性价比 |  1.5元/千次-3.0元/千次  |  1.5元/千次-3.0元/千次  |

#### 2.OCR识别技术
许多公司具有识别证件文字的功能，挑出三家比较突出的，如下所示：

- [百度智能云-文字识别技术-汽车场景文字识别](https://ai.baidu.com/ai-doc/OCR/yk3h7y3ks)
- [腾讯云-文字识别技术-汽车相关识别 Vehicle OCR](https://cloud.tencent.com/product/vehicleocr/details)
- [阿里云-文字识别技术-汽车相关证件识别](https://cloud.tencent.com/document/api/865/36456)

|   对比项  |   百度智能云  |  腾讯云  |  阿里云  |
| ----- | ----- | ----- | ----- |
|   成熟度 |   文档清晰且详细，旗下的API比较细分，能满足多方面的需要；价格最优惠   |   文档较为完善，但涉及到的功能过少 |  使用教程完善、但API文档较不完善；价格较高  |
|   性价比（以驾驶证识别为例） |  25元/千次-40元/次  |  30元/千次-120/千次  |  70.28元/千次  |

### API3使用后风险报告
以下产品均为百度智能云旗下的API工具，且均经过使用与测试。
#### API市场竞争程度

1.车型识别API

- 从搜索结果看，百度云在[bing上的搜索结果](https://cn.bing.com/search?q=%E8%BD%A6%E5%9E%8B%E8%AF%86%E5%88%ABapi&qs=n&form=QBRE&sp=-1&pq=%E8%BD%A6%E5%9E%8B%E8%AF%86%E5%88%ABapi&sc=1-7&sk=&cvid=4BFFB12A77FD413E8BDA1A961F879FFE)为第一名，可以推测其使用面积较其他公司要广
- 从竞争对手看，目前市面上拥有车辆分析api技术的公司数量较少，分别是[百度云](https://ai.baidu.com/ai-doc/VEHICLE/tk3hb3eiv)以及[腾讯云](https://cloud.tencent.com/document/api/865/36456)，二者价格相差无几，但百度云添加了能够显示车辆宽度和高度的特点，从侧面上看功能更齐全

2.车辆外观损伤识别API

- 从具体功能细节上看，百度云的车辆外观识别API为目前市面上比较少有的一类针对[汽车损伤识别的API](https://ai.baidu.com/tech/vehicle/damage)，因此市场竞争力较大。

3.汽车场景文字识别API

- 从性价比看，百度云该API的调用价格（以驾驶证识别为例）为[25元/千次](https://ai.baidu.com/ai-doc/OCR/yk3h7y3ks)，比腾讯云（[30元/千次](https://cloud.tencent.com/product/vehicleocr/details)）以及[阿里云](https://cloud.tencent.com/document/api/865/36456)的价格都要低，性价比更高。

- 从搜索结果看，百度云在[bing上的搜索结果](https://cn.bing.com/search?q=%E9%A9%BE%E9%A9%B6%E8%AF%81%E8%AF%86%E5%88%ABAPI&qs=n&form=QBRE&sp=-1&pq=%E9%A9%BE%E9%A9%B6%E8%AF%81%E8%AF%86%E5%88%ABapi&sc=1-8&sk=&cvid=9765360C4DC44277B5CB2E001A904C84)并不靠前，其搜索率可能并不太占优势。

#### 输入输出限制

1.车型识别API

- 输入：汽车照片
- 输出：汽车的详细信息

2.车辆外观损伤识别API

- 输入：汽车的受损部位照片
- 输出：车辆的受损部件和损伤类型

3.汽车场景文字识别API

- 输入：驾驶证照片
- 输出：驾驶证的信息

#### 定价

1.车型识别API

- 1.5元/千次-3.0元/千次

2.车辆外观损伤识别API

- 1.5元/千次-3.0元/千次

3.汽车场景文字识别API

- 25元/千次-40元/次 

### API4加分项

使用复杂度：已使用3个人工智能API之输入输出，分别是[车型识别API](https://ai.baidu.com/tech/vehicle/car)、[车辆外观损伤识别API](https://ai.baidu.com/tech/vehicle/damage)、[汽车场景文字识别API](https://ai.baidu.com/tech/ocr_cars)
