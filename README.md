# 悟空转发 - MinerProxy

## 项目介绍


-----
 * 专业团队潜心数月打造，励志做最好用最稳定的挖矿转发软件，全新windows服务和控制台分离架构，内置证书，支持TCP和SSL协议，支持任何挖矿内核连接，高性能高并发，独有的服务器异常自动发送短信提醒，全新界面，支持ETH，ETC缺水，稳定不掉线，作者抽水<font color="#dd0000">**`0.25%`**</font>，如果运维开启抽水，作者根据运维抽水比例动态抽水 **`0.5~1%`** 之间，最高不超过**`1%`**，无任何水分，可以自行抓包测试。

-----
## 悟空首创特色功能
   - [x] 节点宕机短信提醒
   - [x] 多节点负载均衡，可按带机量负载也可按顺序负载，宕机自动切换至其它正常节点服务器
   - [x] 潜心研究的客户端加密通道技术
   - [x] 游戏级 socket 网络框架，带机量轻松负载过万连接

## 功能简述
 * 操作系统
   - [x] Windows Server
 * 支持币种
   - [x] ETH
   - [x] ETC
   - [ ] 更多币种支持在开发中，敬请期待...
 * 安全机制
   - [x] <font color="#dd0000">服务端异常短信自动提醒</font>
   - [ ] 更多安全功能将在下个版本开放，敬请期待

------
## [多节点负载均衡实例](ClientExample.md)

## 如何使用
 * 软件界面
   * 服务端
     > ![](/img/主界面.png)
   * 客户端
     > ![](/img/客户端.png)     
 * 下载软件
   * [服务端下载](https://github.com/wukongminer/MinerProxy/releases/download/MinerProxy/server.zip)
   * [客户端下载](https://github.com/wukongminer/MinerProxy/releases/download/MinerProxy/client.zip)
 * 新手指导
   * 开始运行
     > 双击运行【悟空控制台.exe】，如下所示；
     > ![](/img/服务管理.png)
     > 如果启动悟空转发服务成功，此对话框将自动关闭；
   * 添加矿池
     > 单击控制台主界面左上方的<font color="#dd0000">【矿池管理】</font>，在弹出的矿池管理对话框中点击<font color="#dd0000">【添加】</font>，随后在添加矿池对话框中选择对应的币种后再按照提示输入或选择各项矿池参数后点击<font color="#dd0000">【添加】</font>即可，如下图所示：
     > 1、单击矿池管理
     > ![](/img/矿池管理01.png)
     > 2、单击添加
     > ![](/img/矿池管理02.png)
     > 3、输入或选择矿池参数
     > ![](/img/添加矿池.png)
   * 添加钱包
     > 单击控制台主界面左上方的<font color="#dd0000">【抽水钱包】</font>，在弹出的抽水钱包对话框中点击<font color="#dd0000">【添加】</font>，随后在添加钱包对话框中选择对应的币种后再按照提示输入或选择各项钱包参数后点击<font color="#dd0000">【添加】</font>即可，<font color="#dd0000">**`(友情提醒：钱包必须要与矿池绑定，否则会造成抽水不成功)`**</font>，如下图所示：
     > 1、 单击抽水钱包
     > ![](/img/抽水钱包.png)
     > 2、抽水钱包管理
     > ![](/img/抽水钱包01.png)
     > 3、输入或选择钱包详细参数
     > ![](/img/添加钱包02.png)
   * 添加节点
     > 1、单击控制台左上角的【+】添加新节点
     > ![](/img/添加节点01.png)
     > 2、输入或选择节点详细参数
     > ![](/img/添加节点02.png)
     > 3、高级设置下添加节点
     > ![](/img/高级添加节点01.png)
     > ![](/img/高级添加节点02.png)
     > ![](/img/高级添加节点03.png)
     > ![](/img/高级添加节点04.png)
   * 开始挖矿
     > 1、复制转发服务器
     > ![](/img/开始挖矿01.png)
     > 2、查看实时状态
     > ![](/img/查看矿工数据.png)
   * 设置异常接收手机号
     > 1、运行客户端【悟空客户端.exe】
     > ![](/img/客户端01.png)

-------

## 常见问题
   * stratum 协议简介
     > 常用的是有 stratum+tcp 和 stratum+SSL 两种，有些朋友以为用了 stratum+SSL 就是安全的，无法监测得到，这种想法是错误的,stratum+tcp 和 stratum+SSL 只是内容数据包有没有加密的区别，但是用了 SSL 只是数据明文变成了加密数据，其外部特征不变的，且该协议特征明显，只有挖矿才会用到，所以经过大量数据训练，通过机器学习，该协议非常容易就能够被识别
   * 什么是接受数/拒绝数？
     > 接受数: 是指矿机所做的由矿池分发的“任务”中被接受的“任务”数量。
     > 拒绝数: 是指该矿机所做的由矿池分发的“任务”中由于网络延迟等原因没有被接受的“任务”数量。
   * 为什么拒绝率过高？
     > 可能是由于你的服务器与矿池延时过大，请选择服务器与矿池相对应的地区矿池，例如服务器是香港的，那么就近选择亚太地区矿池`(推荐在选择节点时在服务器上PING一下矿池域名，尽量选择延时低的矿池)`
   * 为什么分享出去的服务器其它矿工连接不上
     > 步骤一：Ping 服务器提供商提供的IP地址，看是否通畅;
     > 步骤二：检查下服务器是否开放了端口;
     > 步骤三：检查矿工的协议，注意区别 TCP 和 SSL;
   * 我按照教程添加了节点，完成后为什么控制台上看不到矿工数据
     > 步骤一：检查下转发服务是否正常开启;
     > 步骤二：检查下服务器是否开放了端口;

## 支持我们
  * 为了支持我们后续维护更新，作者抽水: <font color="#dd0000">**`0.1%`**</font>，欢迎各位看官抓包测试。

-------

## 联系我们
 * [官方网站](http://www.wukongzhuanfa.com)
 * [Telegram](https://t.me/wukongminer)
 * [建议与反馈](https://github.com/wukongminer/MinerProxy/issues)
