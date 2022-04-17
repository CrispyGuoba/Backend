# Table of Contents

- Apr 2022: [03 Apr](#Date: 03Apr2022), [09 Apr](#Date: 09Apr2022), [16 Apr](#Date: 16Apr2022), [16 Apr会后](#Date: 16Apr2022会后微信讨论) 




# Date: 16Apr2022 会后微信讨论

@狗跑：

1. 语言： java是国内目前后端主流语言，python不是，应该更加考虑学习成本和应用范围
2. 数据库：和AI共享数据库不现实。后端是online data，AI是offline data，后端业务字段不应该和AI特征值字段耦合。应该使用两个数据库。
3. 技术选型：后端开发应先当成没有AI组，功能需要逐步迭代；并且前期数据不够。
4. 可能需要一个技术上更有经验的人做决策。



@Alice：

经过内部讨论和探讨，决定将语言确定为java，框架spring boot。数据库会在下次和AI、PM的会议中确定。



## Date: 16Apr2022

## 上周任务汇报

- @Alice：上周工作比较忙，这周补上
- @luying(wechat)：fastapi对新手更友好

  - Automatic documentation 
  - No need of postman
  - Data validation
- @shaw: 没有倾向

  - django：功能完善，但响应速度相对慢
  - flask、fastapi：自己开发的部分比较多，但更小巧
- @小舒：

  - django主要支持的是关系型数据库，没有mongodb官方
  - flask数据库支持mongodb
- 锅巴：aws的使用iam身份认证，权限设置
  - 已设置1个30gb，另2个1024GB
  


# Discussion

- @natialia：前端会议做网页，tob toc网页版；第一版会是html
- 数据库的讨论
  - 用什么数据库？
    - 目前来看，我们依旧需要关系型数据库，一对多的关系。
    - @锅巴：不太确定产品给我们的需求，表结构设定。
  
  - 和AI组协作
    - @狗跑：AI 和后端独立，数据库独立。
    - @锅巴：需要考虑怎么调用AI的模型，无论是用tensorflow还是pytorch。
    - @Natalia： Ai组想达到的技术功能，通过照片/视频识别毛色，优化图片的质量，提高动物被领养的几率，推荐算法，领养人的黑名单
  
- CICD

  - @狗跑 的工作经验：
    - 代码部署：先去检测自动执行，代码打包到aws，代码手动上线到k8s
    - git actions 自带详细的文档 链接aws
    - 环境变量：所有可以默认的配置文件，放到github上
- @Natalia：会议记录轮流记录加在同一个文件；github上专门一个文件来装reference links
- @Natalia：四月底五月初，uxui会出结果

## 下周任务

- @Alice：github actions

- @锅巴：aws user；根据CICD文档来部署CICD文档；尝试部署django for testing；
  - 自己的用户组策略分配(权限json)，数据库的权限策略分配，将会和papa协商

- @小舒 & @shaw：学习aws，python后端开发的知识
- @狗跑：在仓库里用github actions打包上传
- jingjing：项目管理留档很重要；团队同频很重要；项目管理工具miro



# Date: 09Apr2022

## 上周任务汇报

- @锅巴：08Apr2022才得到aws的权限打开，接下来继续完善教程
- @Alice：git actions调研
  - Public repository 免费
  - 前端、后端、AI组都需要建立
  - 需要继续调研现有workflow来实现CICD
- @小舒：数据库
  - 上周确定nosql后，比较mongodb 和 dynamoDB

  - dynamoDB：API和mysql比较相似

  - 功能上都可以实现我们的功能，索引上稍微有不同

  - `mongodb`可以用多种`cloud`，但部署上在AWS上会更麻烦

  - 部署在云端都要收费，
    - `mongodb`: pay as you go

    - `dynamodb`: 一开始会更便宜
- @shaw: TPM 确定是先做小程序
  - 前端开发框架：
    - 主流框架：类vue和类react，都支持跨端
      类VUE: uni-app（支持跨端：支付宝/微信）
        使用 Vue.js 开发小程序、H5、App的统一前端框架。  
        *github：https://github.com/dcloudio/uni-app*
      类React: taro
        开源的一款使用 React.js 开发微信小程序的前端框架。
        *github地址：https://github.com/NervJS/taro*
      类Vue: WePY（最近官方更新：2020.6.4）
        *github：https://github.com/Tencent/wepy*
      类VUE: mpvue（已停止维护）
        美团团队开源的一款使用 Vue.js 开发微信小程序的前端框架。（已经停止维护）
        *github地址：https://github.com/Meituan-Dianping/mpvue*
    
  - 问题：小程序前端限制更多，后端没有限制，选择后端需要做哪些考量？



# Discussion

- @Natalia: 要与前端讨论是否一开始使用小程序，应该本周会得出结论
- 小程序前端限制更多，后端没有限制，选择后端需要做哪些考量？
  - 前后端分离的话，不需要考虑平台。
- framework: 既然确定用python，那需要在Django VS Flask选择

- @锅巴：aws 虚拟机 ubuntu: 18.04

## 下周任务

- Luying, Shaw, 小舒：
  - 调研flask和django，记录在hackmd上
  - 数据库调研@小舒：可以和AI组的Jeni姐妹配合调研，如果有必要的话可以协商@Natalia 约一个后端组与AI组的跨组会议
  - 调研flask和django，记录在hackmd
- 锅巴：继续aws部署学习
- Alice: 继续git actions 学习

# Date: 03Apr2022

## 上周任务汇报

- @Shaw

  - 查看了官方文档：完善基本信息进行审核

  - 提交源代码审核

  - 开发语言：前端： 微信自己开发 后端

  - 现有的程序，有很多已有的领养，用户不活跃

- @锅巴：安卓 iOS 官方文档

  - 安卓开发者文档：Kotlin 静态编程语言；运行下载andriod studio 编译， 语言更偏向于java

  - iOS：开发文档，swift；苹果应用商店注册备案

- @小舒：数据库

  - `mongodb`：开发更快，但开源，不限制平台

  - `dynamodb`：`aws`专有，需要继续研究

  - 微信小程序数据库：和`mongodb`差不多

- @Alice：定下aws+k8s的话，我们就需要使用aws的eks

## 本次会议讨论内容

#### 1.  数据库

   - @papa：当数据库确实时，需要和AI组商讨；但需要更倾向于平台不受限的db，just in case of migrating the cloud if necessary.

#### 2. CI/CD:

   - @Alice: 前端后端都需要。

#### 3. peer programming and code review

   - Peer programming: 可以，内部或者邀请senior
   - Code review: 大家都觉得需要
   - @锅巴：也需要代码规范的确定

#### 4. 语言: 

   - AI & 前端更希望python
   - 内部还需等全组人员到齐商讨

#### 5. 第一阶段任务

- @papa：第一个阶段主要是小程序（功能实现）+ webapp（仅显示项目信息）
- @papa：所以现在学习重心可以放在小程序及相关，aws和docker
- @papa：5月初PRD，数据库应该可以明确表头

## 下周任务

- Luying: (未定)
- Shaw：框架
- 小舒：数据库
- 锅巴：aws服务器部署学习，调查在国内部署是否存在问题
- Alice: CICD