![AntiCrawlerSolution](https://github.com/AntiCrawlerSolution/AntiCrawlerSolution/blob/master/Static/%E7%88%AC%E8%99%AB.png)
# :smile:AntiCrawlerSolution(反爬解决方案)

## 一个人在反反爬虫的路上真的很难:cloud::zap::cyclone::snowflake:，不过这里有一群志同道合的我们:umbrella::sunny:

1 . [:mortar_board:写在开头](#1-写在开头)
- 1.1 [:point_right:项目初衷](##1.1-项目初衷)
- 1.2 [:clap:项目介绍](##1.2-项目介绍)
- 1.3 [:wave:加入我们](##1.3-加入我们)
- 1.4 [:muscle:感谢](##1.4-感谢)

2 . [:sunny:反爬分类以及解决方案](#2-反爬分类以及对应解决方案)
- 2.1 [消息头鉴别](##2.1-消息头鉴别)
    - 2.1.1 [Referer鉴别](##2.1.1-字段含义)
        - 2.1.1.1 [反爬原理](##2.1.1.1-反爬原理)
        - 2.1.1.2 [真实场景还原](##2.1.1.2-真实场景还原)
        - 2.1.1.3 [解决方案](##2.1.1.3-解决方案)
    - 2.1.2 [UserAgent鉴别](##2.1.2-UserAgent鉴别)
        - 2.1.2.1 [反爬原理](##2.1.2.1-反爬原理)
        - 2.1.2.2 [真实场景还原](##2.1.2.2-真实场景还原)
        - 2.1.2.3 [解决方案](##2.1.2.3-解决方案)
    - 2.1.3 [Cookie鉴别](##2.1.3-Cookie鉴别)
        - 2.1.3.1 [反爬原理](##2.1.3.1-反爬原理)
        - 2.1.3.2 [真实场景还原](##2.1.3.2-真实场景还原)
        - 2.1.3.3 [解决方案](##2.1.3.3-解决方案)
    - 2.1.4 [基于用户会话(Session)的反爬](##2.1.4-基于用户会话(Session)的反爬)
        - 2.1.4.1 [场景](##2.1.4.1-场景)
        - 2.1.4.2 [原理](##2.1.4.2-原理)
        - 2.1.4.3 [解决方案](##2.1.4.3-解决方案)
        
- 2.2 [IP判别](##2.2-IP判别)
    - 2.2.1 [相同IP鉴别](##2.2.1-相同IP鉴别)
        - 2.2.1.1 [反爬原理](##2.2.1.1-反爬原理)
        - 2.2.1.2 [真实场景还原](##2.2.1.2-真实场景还原)
        - 2.2.1.3 [解决方案](##2.2.1.3-解决方案)

- 2.3 [请求参数、主体判别](##2.3-请求参数、主体判别)
    - 2.3.1 [请求参数鉴别（参数保护）](##2.3.1-请求参数鉴别（参数保护）)
        - 2.3.1.1 [场景](##2.3.1.1-场景)
        - 2.3.1.2 [原理](##2.3.1.2-原理)
        - 2.3.1.3 [解决方案](##2.3.1.3-解决方案)
    - 2.3.2 [请求主体鉴别](##2.3.2-请求参数鉴别)
        - 2.3.2.1 [反爬原理](##2.3.2.1-反爬原理)
        - 2.3.2.2 [真实场景还原](##2.3.2.2-真实场景还原)
        - 2.3.2.3 [解决方案](##2.3.2.3-解决方案)

- 2.4 [验证码判定](##2.4-验证码判定)
    - 2.4.1 [图片验证码](##2.4.1-图片验证码)
        - 2.4.1.1 [反爬原理](##2.4.1.1-反爬原理)
        - 2.4.1.2 [真实场景还原](##2.4.1.2-真实场景还原)
        - 2.4.1.3 [解决方案](##2.4.1.3-解决方案)
    - 2.4.2 [语音验证码](##2.4.2-语音验证码)
        - 2.4.2.1 [反爬原理](##2.4.2.1-反爬原理)
        - 2.4.2.2 [真实场景还原](##2.4.2.2-真实场景还原)
        - 2.4.2.3 [解决方案](##2.4.2.3-解决方案)
    - 2.4.3 [极验验证码](##2.4.3-极验验证码)
        - 2.4.3.1 [反爬原理](##2.4.3.1-反爬原理)
        - 2.4.3.2 [真实场景还原](##2.4.3.2-真实场景还原)
        - 2.4.3.3 [解决方案](##2.4.3.3-解决方案)
    - 2.4.4 [短信验证码](##2.4.4-短信验证码)
        - 2.4.4.1 [鉴别原理](##2.4.4.1-鉴别原理)
        - 2.4.4.2 [真实场景还原](##2.4.4.2-真实场景还原)
        - 2.4.4.3 [解决方案](##2.4.4.3-解决方案)

- 2.5 [用户行为判别](##2.5-用户行为判别)
    - 2.5.1 [页面行为检测](##2.5.1-页面行为检测)
        - 2.5.1.1 [反爬原理](##2.5.1.1-反爬原理)
        - 2.5.1.2 [真实场景还原](##2.5.1.2-真实场景还原)
        - 2.5.1.3 [解决方案](##2.5.1.3-解决方案)
    - 2.5.2 [浏览器指纹检测](##2.5.1-页面行为检测)
        - 2.5.2.1 [反爬原理](##2.5.2.1-反爬原理)
        - 2.5.2.2 [真实场景还原](##2.5.2.2-真实场景还原)
        - 2.5.2.3 [解决方案](##2.5.2.3-解决方案)

- 2.6 [前端反调试Debug](##2.6-前端反调试Debug)
    - 2.6.1 [死循环Debug拦截DevTools](##2.6.1-死循环Debug拦截DevTools)
        - 2.6.1.1 [反爬原理](##2.6.1.1-反爬原理)
        - 2.6.1.2 [真实场景还原](##2.6.1.2-真实场景还原)
        - 2.6.1.3 [解决方案](##2.6.1.3-解决方案)
        
    - 2.6.2 [反无头浏览器（headless）](##2.6.2-反无头浏览器（headless）)
        - 2.6.2.1 [场景](##2.6.2.1-场景)
        - 2.6.2.2 [原理](##2.6.2.2-原理)
        - 2.6.2.3 [解决方案](##2.6.2.3-解决方案)

    - 2.6.3 [前端代码混淆](##2.6.2-前端代码混淆)
        - 2.6.3.1 [场景](##2.6.2.1-场景)
        - 2.6.3.2 [原理](##2.6.2.2-原理)
        - 2.6.3.3 [解决方案](##2.6.2.3-解决方案)


- 2.7 [APP验签](##2.7-APP验签)
    - 2.7.1 [代码混淆](##2.7.1-代码混淆)
        - 2.7.1.1 [反爬原理](##2.7.1.1-反爬原理)
        - 2.7.1.2 [真实场景还原](##2.7.1.2-真实场景还原)
        - 2.7.1.3 [解决方案](##2.7.1.3-解决方案)

- 2.8 [反无头浏览器（Headless）](##2.8-反无头浏览器（Headless）)


3 . [大V推荐](#3-大V推荐)

# 1 写在开头

## 1.1 项目初衷

    创建这个项目的初衷是有几点在日常工作和学习中的感悟：
        （1）接触到的反爬场景少，预先的知识储备不足，真正面对的时候学习周期长，解决难题时间长以致项目延期。
        （2）想要抽空学习，却不知道从哪里入手，没有合适的反爬的社群来交流讨论经验，没有完整可用的案例来辅助学习，网上的案例简单并且基础，不适合想要深入学习的人。
        （3）追求挑战性，这点我想是很多爬虫爱好者的“天性”，正如安全圈子一样，大家总用“英雄主义”的理想，想着没有攻克的难关。所以，就需要新的“难关”抛出，于是，就希望建立这个项目以及相关小组能够帮助大家实现自己的“英雄梦”。
## 1.2 项目介绍

       项目其实很简单，我们会主要分为两个部分，也就是大家通常学习的顺序 - “理论”和“实战”，
       还有一些我们小组自研的开源库，帮助大家平常减少重复造轮子。
       
       理论方面： 我们会总结一下常见的反爬类型以及对应的解决方案、实际案例。
       
       实际案例方面：我们会结合真实的网站，详细的针对其反爬手段来进行分析。 

## 1.3 加入我们

    我们的想法很简单：“正如没有穿不透的墙，也没有反不了的反爬”
    加入我们，反“反爬”开源小组，可以直接加我微信：17610771895来加入我们。
    
## 1.4 感谢

    感谢`@cr`大佬的内容提交

# 2 反爬分类以及对应解决方案

## 2.1 消息头鉴别

### 2.1.1 Referer鉴别

#### 2.1.1.1 字段含义
在HTTP协议中，存在一个`Referer`字段，详情可见[WIKI](https://en.wikipedia.org/wiki/HTTP_referer),当浏览器（或者模拟浏览器行为）向`Web`服务器发送请求的时候，
头信息里有包含`Referer`，这个字段主要有三方面的作用，一是常用来作为网站的流量来源的统计，二是可以用来做防盗链的行为，比如我们的图片服务器只允许我们自己的网站域名来
访问，其他的一概拒绝，第三也是很重要的（ps: 也可以说经常被人利用的一点）就是用来防止恶意请求，很多网站的某些重要页面也会使用这样的机制来识别一些爬虫。

#### 2.1.1.2 真实场景还原

#### 2.1.1.3 解决方案

这个问题的解决方案就是我们需要伪造一个用户的`HTTP`请求头，可以直接打开`chrome`的`DEVTool`，查看`Network`的`tap`，就可以查看到相关的请求头参数。
另外说一下，总结了几种是获取不到`Referer`字段的情况：

（1）在浏览器内直接敲URL
    
（2）windows桌面上的超链接图标
    
（3）浏览器内书签
    
（4）第三方软件（如Word，Excel等）内容中的链接

（5）SSL认证网站跳入

（6）http://example.com/“> meta页面设置自动跳转时，在example.com将取不到REFERER URL

（7）使用JavaScript的Location.href或者是Location.replace()

### 2.1.2 UserAgent鉴别

#### 2.1.2.1 消息头鉴别

`User Agent`中文名为用户代理，简称`UA`，它是一个特殊字符串头，使得服务器能够识别客户使用的操作系统及版本、CPU 类型、浏览器及版本、浏览器渲染引擎、浏览器语言、浏览器插件等,
为什么会有这个字段的鉴别呢，一方面是通过这个字段来判断某个时间段内某个机器的大量请求，另一方面大概就是很多爬虫框架或者各个语言请求库直接访问网站的话`UA`字段都会显示语言的版本或者
是框架的版本，所以这个参数还是会过滤很多小白爬虫。

#### 2.1.2.2 真实场景还原



#### 2.1.2.3 解决方案

这个问题的解决方案也是通过使用伪造`HTTP`请求头的方式来伪造你的请求，参考资源有几下几种：

[常用的请求头](http://www.cnblogs.com/zrmw/p/9332801.html)

很多人可能都不太理解`UA`头里面的各个子参数的含义，下面这个网站可以让大家来了解一下

[UA解析](http://www.atool.org/useragent.php)

### 2.1.3 Cookie鉴别

#### 2.1.3.1 消息头鉴别

反爬界最喜欢用的两种反爬手段其一，`Cookie`鉴别大多会出现在某些需要登录的网站，因为此类网站的信息都是高度信息化或者原创化，所以不想轻易的被爬取和提高用户依赖性，他们就会需要用户登录，
这个时候我们就必须要登录来获取登录之后用户的`Cookie`，这个字段是用来识别用户的身份的，一般服务端也会根据这个字段会用户展示不同的页面，所以可能你是否使用
`Cookie`显示的是不同的页面。

#### 2.1.3.2 真实场景还原

#### 2.1.3.3 解决方案

解决`Cookie`的方法最简单的还是伪造请求头，也就是需要我们先登录网站，然后获取的到具体的`Cookie`的值，一般来说`Cookie`的有效期都会有一定的时间，过期之后我们再按
之前的方法获取`Cookie`，这一部分会涉及到一部分自动化登录的原理，这个我们会结合实际的场景来谈，这一部分我们需要知道伪造请求头就能绕过`Cookie`鉴别。

我们这有几种方法告诉大家怎么分析`Cookie`:

(1) 删除`Cookie`看是否正常，另外关于`Cookie`的反爬我们需要把每次环境给配置好，也就是为了防止一些网站根据我们之前的历史登录账号来判断我们是否具有反爬特征，比如我用浏览器
频繁注册账号并登录，这样的话会在历史纪录，账号记录中留下`痕迹`，所以我们每次测试最好使用浏览器的`隐私模式`，因为这种模式都会有一个`DNT`头，也就是拒绝对方网站对于己方的追踪，
另外，我们在切换账号的时候需要清空历史记录。

（2）我们需要拿多个页面测试，也就是我们访问多个页面，看看`Cookie`的值是否是变化的，如果是不变的话，可能它只是一个登录的凭证，如果它是变化的，我们就得具体看看是哪个参数变化的具体分析了。

（3）找到Cookie中比较特别的词（至于什么是特别的词，需要大家用正常人的智商去判断）。用这个词去主要的Javascript文件中搜索。一般来说会找到文件中具体是哪一句设置的，如果这个逻辑看着很复杂，可以在这一句打断点调试来判断这个Cookie到底如何生成的。 

（4）终极方案Break-on-Access

 关于这个Chrome Snippets怎么使用，大家直接参考这个这个[Github](https://github.com/paulirish/break-on-access)的链接，解释的挺清楚。有了这个工具，我们调用一下：

breakOn(document, 'cookie');

就可以在任何语句修改Cookie的时候，进入断点。再通过单点调试，逐步揭开反爬工程师险恶的面纱了。 

### 2.1.4 基于用户会话(Session)的反爬

#### 2.1.4.1 场景
一般中小网站为了减轻数据库的压力，不会把请求次数记录在数据库中，因为每次请求都得update，对数据库压力相对较大，这类站点会选择把请求次数记录在会话数据中。
#### 2.1.4.2 原理
在用户session中记录请求频次，同时记录封禁次数，单次封禁时间可以跟封禁次数指数相关，以此限制单账户的请求频率。
#### 2.1.4.3 解决方案

这种方式的弱点在于，会话数据只对一次会话有效，通常用户访问web服务器时，服务器会颁发一个session_id，通过cookie发送给用户，用户只要触发封禁前清空cookie，重新建立会话就可以了。对于不需要登录的场景，还可以不带cookie（session_id）去请求服务器。

------

## 2.2 IP判别

### 2.2.1 相同IP鉴别

#### 2.2.1.1 消息头鉴别

反爬界最喜欢用的两种反爬手段其二，说到`IP`来反爬，真的让一些小公司或者说一些小的爬虫小组无可奈何，特别是需要爬的网站需要高频访问，并且对于`IP`审查很严格的时候，`IP`成了一个难题

#### 2.2.1.2 真实场景还原

#### 2.2.1.3 解决方案

目前解决`IP`短缺的问题就是维护`IP`池，所以我们的方案就围绕`IP`池来说，

（一）开源`IP`池，也就说我们可以爬取一些代理`IP`的网站，因为这类网站都会有一些免费的可试用的`IP`，具体情况可以参考[代理ip网站情况分析]https://www.jianshu.com/p/6e5f35aa0e04,
`IP`池的实现方法大家可以参考几个大佬自己做的`IP`池：

（1）[七夜大佬](https://github.com/qiyeboy/IPProxyPool)

（2）[另一位大佬](https://github.com/jhao104/proxy_pool)

（二）召集全公司，在你们公司所有云服务器上部署好`http`和`ss`代理，这样有两点好处，一方面公司越大，`IP池`越大，另一方面，其实你们的服务器上部署的正式的网站、APP服务也会让你们的`IP`变得比别人稳定、可靠，稍微降低被封的风险，不过要全公司都这么搞，有点麻烦。

（三）去我们第一步说的那些代理网站买服务，不过得"擦亮眼睛看好了"

------

## 2.3 请求参数、主体判别

### 2.3.1 请求参数鉴别（参数保护）

#### 2.3.1.1 场景

web的参数保护，主要用于表单防护，特别是注册和登录表单的防护，我们知道有效提供攻击成本的手段主要是基于IP的计数和基于用户的计数，其中基于用户的计数，攻击者会批量注册账号，因此注册和登录表单的保护变得尤其重要

#### 2.3.1.2 原理

参数保护主要依赖参数加密和混淆
参数加密主要是用JS加密表单需要提交的数据，后端解密这个数据。
加密方式很多，有单个参数加密的，也有所有参数整体加密的。
如果是单个参数加密的，不仅可以加密参数值，还可以加密参数名，还可以随机填充一些隐藏的input。
表单里的input数量随机，参数值随机，参数名也是随机的。然后利用JS控制DOM显示出真正有效的input。
这些JS代码通常会被保护起来。见[前端代码混淆](##2.6.2-前端代码混淆)

#### 2.3.1.3 解决方案

对于非动态的表单，可以逆向JS代码。
对于动态的表单，通常需要上headless浏览器

PS: 关于`headless`浏览器，现在主要推荐`google-chromium` 可以使用 `Remote debugging protocol`以及其相对应的高层封装[puppeteer](https://github.com/GoogleChrome/puppeteer)

### 2.3.2 请求主体鉴别

#### 2.3.2.1 消息头鉴别

#### 2.3.2.2 真实场景还原

#### 2.3.2.3 解决方案

------

## 2.4 验证码判定

### 2.4.1 图片验证码

#### 2.4.1.1 反爬原理

#### 2.4.1.2 真实场景还原

#### 2.4.1.3 解决方案

图片验证码目前算是最简单，最常见的验证码了，因此对于它的破解手段也是比较常见，“烂大街”了，图片验证码的难度系数划分大致是由其图片中图案的复杂程度来划分，比如：

1.数字类或字母类

2.数字字母混合类

3.数字字母混合乱序类

4.物品识别类

对于不同难度的有不同种的解决方案，之后会详细补充。

### 2.4.2 语音验证码

#### 2.4.2.1 反爬原理

#### 2.4.2.2 真实场景还原

#### 2.4.2.3 解决方案

### 2.4.3 极验验证码

#### 2.4.3.1 反爬原理

#### 2.4.3.2 真实场景还原

#### 2.4.3.3 解决方案

### 2.4.4 短信验证码

#### 2.4.4.1 鉴别原理

一般短信都会需要一个手机号，鉴别的原理也是基于此，这类鉴别方式也是将我们之前的`Cookie`鉴别结合在一起，首先需要能有接收验证码的手机，注册账号，之后才会轮到自动化登录那一步，
所以我们要想注册大量手机号，类似“刷单”，我们就需要大量手机号。

#### 2.4.4.2 真实场景还原

#### 2.4.4.3 解决方案

这个问题的解决方法大体如上面的图片验证码那样，算是比较普遍了，因为现在有很多手机接码平台，类似[易码](http://www.51ym.me/User/Default.aspx)这样算是比较稳定的平台，大概资费在0.1元/条这样，原理大家可以自行百度“猫池”，之后会给大家一个大致的分析。

------

## 2.5 用户行为判别

### 2.5.1 页面行为检测

#### 2.5.1.1 消息头鉴别

#### 2.5.1.2 真实场景还原

#### 2.5.1.3 解决方案

### 2.5.2 浏览器指纹检测

#### 2.5.2.1 消息头鉴别

#### 2.5.2.2 真实场景还原

#### 2.5.2.3 解决方案

-----

## 2.6 前端防护

### 2.6.1 死循环Debug拦截DevTools

#### 2.6.1.1 消息头鉴别

#### 2.6.1.2 真实场景还原

#### 2.6.1.3 解决方案

### 2.6.2 反无头浏览器（Headless）

#### 2.6.2.1 场景

#### 2.6.2.2 原理

#### 2.6.2.3 解决方案

### 2.6.3 前端代码混淆

#### 2.6.3.1 场景

#### 2.6.3.2 原理

#### 2.6.3.3 解决方案

------

## 2.7 APP验签

### 2.7.1 代码混淆

#### 2.7.1.1 消息头鉴别

#### 2.7.1.2 真实场景还原

#### 2.7.1.3 解决方案

# 3 大V推荐

### 验证码相关： 
    
[冷月的博客](https://lengyue.me/)

### Js逆向分析： 
    
[dust的博客](https://blowingdust.com/)

### 脱壳破解相关：
    
[吾爱破解](https://www.52pojie.cn/forum-5-1.html)

### 安全相关： 
    
[zzh](https://www.zzhsec.com)
[freebuf](https://www.freebuf.com/)
