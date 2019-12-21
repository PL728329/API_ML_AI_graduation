# 毕业纪念册小程序PRD文档

## （一）背景
- 小海是一名已经工作两年的上班一族，在繁华而又匆忙的都市生活中，小海经常怀念以前读大学时在大山里与朋友们一起惬意玩乐的时光，在一次节假日里，小海想约以前的同学们一起组织一次团建活动，联络感情。但是小海的几个至亲好友都不在小海所在的地方工作，不能赴约，可是小海朋友圈里的大学同学又那么多，不能够确定谁跟小海同城，于是小海打开了毕业纪念册小程序，里面有一个同城定位功能，小海通过这个功能，找到了同城的同学一起吃了饭，通过刷脸查看了跟这些同学以前拍过的照片，还将吃饭拍的自拍又上传至毕业纪念册小程序。就这样，小海度过了美好的假日时光，结束假期后，她又动力满满的投入到了工作中。


## （二）加值宣言
- 孤独是年轻人的通病，尤其是生活在大都市里的年轻人，孤独似乎已经成为生活的常态。那些常年独居生活的年轻人，更是被媒体贴切地称为“空巢青年”，他们离群索居的生活状态正受到社会越来越多的关注。开设毕业纪念册小程序想解决的其中一个痛点就是缓解年轻人的“孤独感”。而我们将会利用Microsoft的人脸识别API以及高德地图定位API对毕业纪念册小程序进行加值和优化。
- 核心：利用Microsoft的人脸识别API，让用户在使用该小程序时可以通过刷脸就快速找到与自己相关的照片而不用费劲翻找。
- 重要：运用了高德地图定位API，可以找出与自己同城的小伙伴一起组织活动。


## （三）核心价值（最小可行性产品）
- 用人脸识别服务解决用户翻找旧照不够快捷、简便的问题，同时提供定位服务方便用户联络。


## （四）目的
- 让你们不再做“最熟悉的陌生人”——毕业纪念册小程序

## （五）目标
- 前期目标

  1. 通过刷脸，查找与自己相关的照片。
  2. 可以上传几个同学/朋友之间的相关照片。

- 后期目标
  1.  点击相关用户头像，可以查看用户大致定位。

## （六）用户
- 毕业生，联谊爱好者，毕业1-3年的工作一族。


## （七）用户痛点
- 场景一：毕业后想将各类毕业纪念照统一保存起来，方便日后查看。
- 场景二：路上遇到大学同学，吃完饭后疯狂自拍后想找个地方将照片存起来，节省手机空间。
- 场景三：节假日想约旧时同学出来玩，但并不是所有同学都在你这个城市工作，一个一个问实在是太麻烦。
- 场景四：跟三两好友想看以前的某些照片时，因为照片实在是太多了，一时半会找不完，浪费时间怎么办？

## （八）用户需求（使用的人工智能要反映到列表当中）
| 用户案例 | 对应功能 | 重要程度 |
:---:|:---:|:---:|
| 用户想快速找到与自己有关的照片 | 人脸识别功能 | 重要 |
| 用户想查看他人定位 | 普通IP定位功能 | 重要 |

### 具体应用场景
- 场景一：一次节假日里，小海想约以前的同学们一起组织一次团建活动，联络感情。但是小海的几个至亲好友都不在小海所在的地方工作，不能赴约，可是小海朋友圈里的大学同学又那么多，不能够确定谁跟小海同城。于是小海打开了毕业纪念册小程序，里面有一个同城定位功能，小海通过这个功能，找到了同城的同学一起吃了饭。

- 场景二：小海在同学聚会中通过刷脸查看了跟这些同学以前拍过的照片，还将吃饭拍的自拍又上传至毕业纪念册小程序，更新了在毕业纪念小程序中自己的纪念相册，与朋友们又多了一份回忆。

## （九）使用者交互与设计（axure产品原型）
- 产品结构图：
![产品结构图](https://github.com/PL728329/API_ML_AI_graduation/blob/master/images/%E6%AF%95%E4%B8%9A%E7%BA%AA%E5%BF%B5%E5%86%8C%E5%B0%8F%E7%A8%8B%E5%BA%8F%E2%80%94%E4%BA%A7%E5%93%81%E7%BB%93%E6%9E%84%E5%9B%BE.png)

- 功能结构图：
![功能结构图](https://github.com/PL728329/API_ML_AI_graduation/blob/master/images/%E6%AF%95%E4%B8%9A%E7%BA%AA%E5%BF%B5%E5%86%8C%E5%B0%8F%E7%A8%8B%E5%BA%8F%E2%80%94%E2%80%94%E5%8A%9F%E8%83%BD%E7%BB%93%E6%9E%84%E5%9B%BE.png)

- 信息结构图：
![信息结构图](https://github.com/PL728329/API_ML_AI_graduation/blob/master/images/%E6%AF%95%E4%B8%9A%E7%BA%AA%E5%BF%B5%E5%86%8C%E5%B0%8F%E7%A8%8B%E5%BA%8F%E2%80%94%E2%80%94%E4%BF%A1%E6%81%AF%E7%BB%93%E6%9E%84%E5%9B%BE.png)

## （十）API的运用（使用水平）
#### 百度地图开放平台-普通ip定位api
- 描述：利用IP获取大致位置，调用API接口，返回请求参数中指定上网IP的大致位置信息（一般为城市级别），位置信息包括：经纬度、省、市等地址信息。（普通IP定位服务目前不支持海外场景。）
- 请求URL：
  1. //HTTP协议 http://api.map.baidu.com/location/ip
  2. //HTTPS协议 https://api.map.baidu.com/location/ip

- 输出：
```
{  
    address: "CN|北京|北京|None|CHINANET|1|None",    #详细地址信息  
    content:    #结构信息  
    {  
        address: "北京市",    #简要地址信息  
        address_detail:    #结构化地址信息  
        {  
            city: "北京市",    #城市  
            city_code: 131,    #百度城市代码  
            district: "",    #区县  
            province: "北京市",    #省份  
            street: "",    #街道  
            street_number: ""    #门牌号  
        },  
        point:    #当前城市中心点  
        {  
            x: "116.39564504",    #当前城市中心点经度
            y: "39.92998578"    #当前城市中心点纬度
        }  
    },  
    status: 0    #结果状态返回码  
}
```
- 百度普通ip定位测试结果：
- 代码输入：
![代码输入](https://github.com/PL728329/API_ML_AI_graduation/blob/master/images/%E6%AF%95%E4%B8%9A-%E7%99%BE%E5%BA%A6.png)

- 代码输出：
![代码输出](https://github.com/PL728329/API_ML_AI_graduation/blob/master/images/%E6%AF%95%E4%B8%9A-%E7%99%BE%E5%BA%A6%E7%BB%93%E6%9E%9C.png)

---
#### 高德开放平台-ip定位api
- 描述：IP定位是一个简单的HTTP接口，根据用户输入的IP地址，能够快速的帮用户定位IP的所在位置。
- 请求URL：https://restapi.amap.com/v3/ip?parameters
- 请求方式：GET
- 输出：
```
{
"status" :
"1",
"info" :
"OK",
"infocode" :
"10000",
"province" :
"北京市",
"city" :
"北京市",
"adcode" :
"110000",
"rectangle" :
"116.0119343,39.66127144;116.7829835,40.2164962"
}
```
- 高德ip定位测试结果：
![测试结果](https://github.com/PL728329/API_ML_AI_graduation/blob/master/images/%E6%AF%95%E4%B8%9A-%E9%AB%98%E5%BE%B7.png)

---
#### Microsoft azure-人脸识别api
- 描述：
  1. 检测并比较人脸；
  2. 基于相似度将图像组织成组；
  3. 识别图像中先前标记的人物
  4. 在本地或在云中运行；
- 输入：
```
import requests
import json

# set to your own subscription key value
subscription_key = None
assert subscription_key

# replace <My Endpoint String> with the string from your endpoint URL
face_api_url = 'https://<My Endpoint String>.com/face/v1.0/detect'

image_url = 'https://upload.wikimedia.org/wikipedia/commons/3/37/Dagestani_man_and_woman.jpg'

headers = {'Ocp-Apim-Subscription-Key': subscription_key}

params = {
    'returnFaceId': 'true',
    'returnFaceLandmarks': 'false',
    'returnFaceAttributes': 'age,gender,headPose,smile,facialHair,glasses,emotion,hair,makeup,occlusion,accessories,blur,exposure,noise',
}

response = requests.post(face_api_url, params=params,
                         headers=headers, json={"url": image_url})
print(json.dumps(response.json()))
```
- 输出：
  1.太长省略，请看结果。

- Microsoft azure人脸识别结果：
- 代码输入：
![代码输入](https://github.com/PL728329/API_ML_AI_graduation/blob/master/images/Microsoft%E4%BA%BA%E8%84%B8-%E4%BB%A3%E7%A0%81.png)
- 代码输出：
![代码输出](https://github.com/PL728329/API_ML_AI_graduation/blob/master/images/Microsoft%E4%BA%BA%E8%84%B8-%E4%BB%A3%E7%A0%81%E8%BE%93%E5%87%BA.png)

- 单张人脸：
![单张人脸测试结果](https://github.com/PL728329/API_ML_AI_graduation/blob/master/images/Microsoft-%E4%BA%BA%E8%84%B8%E8%BE%93%E5%85%A5.png)

- 不同人脸：
![不同人脸测试结果](https://github.com/PL728329/API_ML_AI_graduation/blob/master/images/Microsoft-%E4%B8%8D%E5%90%8C%E4%BA%BA%E8%84%B8.png)

- 多人人脸输入：
![多人人脸测试结果](https://github.com/PL728329/API_ML_AI_graduation/blob/master/images/Microsoft-%E5%A4%9A%E4%BA%BA%E4%BA%BA%E8%84%B8%E8%BE%93%E5%85%A5.png)

---
## （十一）API使用比较分析
- 高德地图开放平台-IP定位api：
  1. 针对基础服务api有每日免费调用量的限制；
  2. API调用文档清晰，相对同类API来说更容易上手；
  3. 针对中小型企业使用需求推出流量包（30元/万次），可以按需购买；
  4. 针对大型企业使用需求推出流量包月（60000元/月），不限流量，使用无忧；
  5. [价格文档](https://lbs.amap.com/home/package?active=quota)

- 百度地图开放平台-普通IP定位api：
  1. 每天有免费的配额及并发量次数。若超出用量，则需单独联系客服提升配额与并发量上限；
  2. 一般用户配额上限为0.1万次/天（1000次/天），并发量：1QPS（最高并发量为10QPS）；
  3. 可以确定大致位置，一般为城市中心点。位置信息包括经纬度、省、市等信息；
  4. 普通IP目前不支持海外场景；
  5. [价格文档](http://lbsyun.baidu.com/apiconsole/auth/privilege)

- Microsoft azure-人脸识别api：
  1. API文档清晰明了，比较容易上手；
  2. 识别速度较快，置信度也比较高（单人来说）；
  3. [价格文档](https://azure.microsoft.com/zh-cn/pricing/details/cognitive-services/)

## （十二）人工智能概率性
- 人脸识别可能会出现的问题：
  1. 环境问题，无法成功识别用户的脸；
  2. 姿态问题，用户识别脸部时姿势不正，导致识别不成功；
  3. 遮挡问题，用户进行识别时，不小心或是有眼镜等物体遮挡脸部，可能会导致识别失败；

- 解决办法：
  1. 加强机器自身的深度学习；
  2. 进行算法优化（详见：[如何提高人脸检测正确率](https://blog.csdn.net/u010402786/article/details/52261933)）

## （十三）API使用风险评估
- 人脸识别api：
  1. 市场竞争度：现阶段人脸识别的应用领域非常广泛，但同时其行业市场竞争也比较激烈。目前，我国人脸识别领域主要有以云从、商汤等四大独角兽为首的初创公司，海康威视、佳都科技等上市公司和腾讯、阿里巴巴、百度为首的互联网巨头三个大阵营。
  2. 未来发展性：我国人口规模巨大，经济增长迅速，对可靠的人脸识别技术的各方面需求越来越迫切。一旦人脸识别得以推广，人工智能和人机交互成为人脸识别下一个商业爆发点，其发展潜力与前景将十分美好。
