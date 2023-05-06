# Linds

<p align="center">
  <img width="144" src="https://raw.githubusercontent.com/lindsec/Linds/main/img/linds.jpg">
</p>


#### 介绍
**Linds是一款开源的专注Linux安全方向的综合平台。**

Linds集多种防火墙、重点日志分析、机器深度学习、AI异常检测等为一体，用算法对抗未知攻击做为重点，
以数据保护和未知漏洞发现为核心，对管理员零信任重点审计，及时发现数据异常和泄露。

<br>

#### 初衷
数字经济数据作为关键生产要素，重要性大幅提升，同时数据泄露不仅给企业带来千百万甚至上亿的经济损失，更给社会带来无法评估的安全隐患。

暗网上45亿条中国个人信息泄露说明：90%以上的黑客组织热衷于攻击关键政府部门、大中型企业，获取重要的数据以达到其经济诉求或者破坏，
另外数据在员工、合作组织之间流通，也很容易造成数据泄露。

黑客一般通过两种方式获取重要数据：<br>
1、利用WEB API或未知RCE漏洞在服务器上安装后门。现在高级漏洞都不直接公开了，上升为国家之间情报战略，秘密潜伏窃取数据比搞破坏的更多。<br>
2、通过钓鱼控制了管理员电脑，通常手段是发送带有POC攻击的简历、商务合作邮件等各种社会工程学套路给单位内部人员，一打开就中招木马，
从而进一步利用内网电脑做跳板获取重要数据，防不胜防。

<br>

#### 功能
<table cellspacing="0" cellpadding="0">
  <thead>
    <tr>
      <td align="center">模块名称</td><td align="center">特色功能</td><td align="center">解决问题</td>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td valign="middle">物理安全</td>
      <td valign="middle">监控CPU/内存/磁盘，记录TOP5进程</td>
      <td valign="middle">发现异常占资源进程，保障硬件安全</td>
    </tr>
    <tr>
      <td valign="middle">流量安全</td>
      <td valign="middle">用AI监控所有流量/连接数等</td>
      <td valign="middle">发现异常流量/DDOS/攻击/数据泄露</td>
    </tr>
    <tr>
      <td valign="middle">SSH安全审计</td>
      <td valign="middle">监控SSH登录和命令操作日志</td>
      <td valign="middle">审计系统管理员操作日志，发现高危行为，保障SSH安全</td>
    </tr>
    <tr>
      <td valign="middle">WEB应用防火墙</td>
      <td valign="middle">用规则、智能语义解析解决CC、漏洞扫描、SQL注入、爬虫、发现未知攻击</td>
      <td valign="middle">保障WEB安全</td>
    </tr>
    <tr>
      <td valign="middle">进程防火墙</td>
      <td valign="middle">用AI监控所有进程流量/IP详情</td>
      <td valign="middle">及时发现木马、高危进程数据泄露等</td>
    </tr>
    <tr>
      <td valign="middle">文件防篡改</td>
      <td valign="middle">监控/etc/配置、开机启动等重点文件</td>
      <td valign="middle">及时发现木马、高危文件修改行为</td>
    </tr>
    <tr>
      <td valign="middle">定制功能</td>
      <td valign="middle">按客户需求</td>
      <td valign="middle">按客户需求</td>
    </tr>
  </tbody>
</table>

**tips：直接安装服务器，将流量、防火墙、进程、日志完美统一，有效守住服务器防御的第一道（防火墙）和最后一道关口（日志审计），保障服务器数据安全。**
<br>
<br>

#### 进程防火墙

用机器深度学习检测每个联网进程的服务端口、访问IP、流量进出、协议类型（TCP/UDP/ICMP）等，及时异常流量/木马等风险进程泄露数据。<br>
1、 全程记录服务器每个进程的IP、进出流量、在线时长等数据。<br>
2 、用AI技术分析危险进程，异地IP/异常流量/危险行为等将报警。<br>
3 、黑白名单模式阻断进程，防止服务器被未知漏洞植入木马后门通信。<br>
<p align="center">
  <img src="https://raw.githubusercontent.com/lindsec/Linds/main/img/2-2.jpg">
</p>

<br>

#### SSH安全审计

很大一部分数据泄露是技术人员的电脑被植入了后门，再利用管理员电脑作为跳板，连接服务器，获取数据。<br>
1、 全面审计用户如root的操作命令，对任何终端都不信任，危险指令、删除日志、异常、异地登录等实时报警。<br>
2 、全面防御对SSH服务的扫描探测、密码破解等。<br>
3 、详细的日志和威胁统计分析。<br>
<p align="center">
  <img src="https://raw.githubusercontent.com/lindsec/Linds/main/img/2-3-1.jpg">
</p>
<p align="center">
  <img src="https://raw.githubusercontent.com/lindsec/Linds/main/img/2-3-2.jpg">
</p>

<br>

#### WEB应用防火墙

有很大一部分数据记录是通过WEB API漏洞或者WEBSHELL，绕过系统权限访问和拉取数据。<br>
1、具有独立商业WEB应用防火墙完整功能，包括机器学习、智能语义分析引擎等。<br>
2、全面记录WEB每个URL的访问次数、攻击日志、流量统计等。<br>
3、用算法重点对抗webshell和未知漏洞，及时发现WEB异常行为导致的数据泄露。<br>
<p align="center">
  <img src="https://raw.githubusercontent.com/lindsec/Linds/main/img/2-4.jpg">
</p>

<br>

#### 文件防篡改

保护重要的目录如/etc/rc.d，一旦文件发送改动，及时报警。

<br>

#### 物理安全

每隔1分钟记录系统CPU、内存、磁盘等占用情况，记录最占资源的TOP5进程名称，异常行为如CPU飙升等报警。

<br>

#### 流量安全

记录并监控系统流量，一旦发现异常，则报警。

<br>

#### 演示地址

演示地址（请用大屏电脑观看，带宽很小，首次访问需要10秒）：<br>
http://59.110.1.135:9998/proc.html <br>
非最终产品，新模块和功能整合还在研发中。<br>

<br>

#### 联系方式

微信：qq1510837410 <br>
qq：1510837410 <br>
邮件：1510837410@qq.com <br>
