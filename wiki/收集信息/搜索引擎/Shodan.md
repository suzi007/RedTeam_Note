网址：[https://www.shodan.io](https://www.shodan.io/)

活动：Shodan黑五1美元一个，淘宝、咸鱼可以看看

普通：69美元 每月最多 100 万个结果 每月扫描多达 5,120 个 IP 5,120 个 IP 的网络监控

高级：359美元 每月最多 2000 万个结果 每月扫描多达 65,536 个 IP 65,536 个 IP 的网络监控

超级：1099元 每月无限 每月扫描多达 327,680 个 IP 327,680 个 IP 的网络监控

普通与高级功能差别：漏洞搜索过滤器

### 语法

- city：搜索指定城市 例如：city:“tokyo ”
- country：搜索指定国家 例如：country:“JP”
- http.title：搜索指定网站标题 列如：http.title:“hacked by”
- http.html：搜索指定网页类容 例如：http.html:“hello world”
- http.status：搜索指定返回响应码 例如：http.status:“200”
- http.server：搜索指定返回中的server类型 例如：http.server:“PHP”
- net：搜索指定网络范围或 IP段，例如：net:“8.8.0.0/16”
- org：搜索指定的组织或机构，例如：org:“google”
- port：搜索指定的端口或服务，例如：port:“22”
- product：搜索指定的操作系统/软件/中间件，列如：product:“Samsung”
- screenshot.label：搜索指定描述图像内容的标签 列如：screenshot.label:“ics”
- os：搜索指定限定系统OS版本， 例如：os:“Windows Server 2008 R2”
- hostname：搜索指定的主机或域名，例如：hostname:“google”
- vuln：搜索指定CVE漏洞编号，例如：vuln:“CVE-2014-0723”
- isp：搜索指定的ISP供应商，例如：isp:“China Telecom”
- version：搜索指定的软件版本，例如：version:“1.2.3”
- geo：搜索指定的地理位置，参数为经纬度，例如：geo:“44.55,66.77”

### 搜索案例

###搜索日本国家，中间件是Apache服务器并且状态码是200的机器

country:"JP" && apache && http.status:"200"

###搜索日本国家，摄像头是海康威视

country:"JP" && Hikvision-Webs

###搜索日本国家，操作系统是Windows Server 2008 R2并且开放3389端口的机器

country:jp && os:Windows Server 2008 R2 && port:3389

###搜索日本国家，操作系统是Windows Server并且存在永恒之蓝漏洞的机器(更高级会员才能使用vuln)

country:jp && os:Windows Server * && vuln:CVE-2017-0146