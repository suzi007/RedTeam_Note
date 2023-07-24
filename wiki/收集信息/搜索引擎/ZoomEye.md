免费： 查询结果展示量：4百条 查询API额度：每月1w

高级：4800/年 查询结果展示量：1千条 查询API额度：每月3w

VIP：9600/年 查询结果展示量：2千条 查询API额度：每月4w

高级与VIP功能差别：蜜罐识别

### 语法

- country：搜索指定国家 例如：country:“JP”
- city：搜索指定城市 例如：city:“San Diego”
- [subdivisions](https://www.zoomeye.org/searchResult?q=subdivisions:)：搜索相关指定行政区的资产 例如：subdivisions:“东京”
- [ssl.cert.availability](https://www.zoomeye.org/searchResult?q=ssl.cert.availability:1)：搜索证书是否在有效期内 例如：ssl:“1”or“0”
- ip：搜索指定的IP(ipv4/6) 列如：[ip:](https://www.zoomeye.org/searchResult?q=ip:)“8.8.8.8”
- cidr：搜索指定的IP段 列如：[cidr:](https://www.zoomeye.org/searchResult?q=cidr:52.2.254.36/24)“52.2.254.36/24”
- org：搜索指定的组织或机构，例如：org:“google”
- isp：搜索相关网络服务提供商的资产 例如：[isp:](https://www.zoomeye.org/searchResult?q=isp:)“China Mobile”
- port：搜索指定的端口或服务，例如：port:“22”
- hostname：搜索相关IP"主机名"的资产 例如：[hostname:](https://www.zoomeye.org/searchResult?q=hostname:google.com)“google.com”
- site：搜索域名相关的资产 例如：[site:](https://www.zoomeye.org/searchResult?q=site:baidu.com)“baidu.com”
- device：搜索路由器相关的设备类型 例如：[device:](https://www.zoomeye.org/searchResult?q=device:)“router”
- os：搜索指定限定系统OS版本， 例如：os:“Windows Server 2008 R2”
- title：搜索指定网页类容 例如：[title:](https://www.zoomeye.org/searchResult?q=title:)“hello world”
- app：搜索指定的组件 列如：app:“apache ”
- ver：搜索指定的版本 l例如：ver“1.2.3”
- service：指定服务类型 例如：service:“ftp”