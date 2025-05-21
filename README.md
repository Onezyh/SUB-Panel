## 使用方法一：Fork仓库 [视频教程](https://youtu.be/B4pBQHWgvfw)
1. 直接`Fork`本存储库。本存储库`main`主线默认为`自动升级为最新版本`。
2. 到`Cloudflare`利用`Pages+github`搭建。
3. 再增加下面必要的变量。
## 使用方法二：自建仓库(独一混淆代码) [视频教程](https://youtu.be/sWy9gCBA5Lo)
1. 新建一个私人仓库，项目可随意命名，但要避开 BPB 敏感词。
2. 在该项目创建`.github/workflows/Obfuscate.yml`。
3. 复制`创建仓库源码.js`的代码，粘贴到项目，保存。
4. 点击`Obfuscate.yml`旁边的小黄点同步到 BPB 代码，同步完成生成`_worker.js`与`origin.js`。如果找不到小黄点，请前往：`你的项目`→`Actions`→左边的`Build Obfuscate BPB Panel`→中间的`Build Obfuscate BPB Panel`的工作流文件是否有效。
7. 到`Cloudflare`里创建`Pages+github`，找到刚刚的 github 项目，用其创建 Pages 项目，并修改下面的变量及绑定 kv 空间。
8. 引用请注明出处：[SO启程Github](https://github.com/Setout8/Book-Pen-Book)。

## 环境变量与说明
| 变量  | 用法 |
| :-------------: | :-------------: |
| **UUID**  | 必要；[在线生成](https://1024tools.com/uuid) ，用于生成 VLESS 节点配置 |
| **PROXY_IP**  | 必要；旧版本是`PROXYIP`，[查是否有效](https://www.nslookup.io/domains/ts.hpc.tw/dns-records/#cloudflare)  |
| **TR_PASS**  | 必要；密码，用于生成 Trojan 节点配置  |
| **kv**  | 必要；KV命名空间  |
| **/panel**  | 在 url 后面增加/panel访问面板  |
| **SUB_PATH**  | 订阅的 URI  |
| **FALLBACK**  | 后备域 |
| **DOH_URL**  | 核心 DOH |
1. 代理IP的变量：v3.1.4 及以下称为旧版本为`PROXYIP`，v3.2.0 及以上版本为`PROXY_IP`。
2. 来自大佬分享的PROXYIP：`proxy.xxxxxxxx.tk`、`edgetunnel.anycast.eu.org`、`ts.hpc.tw`、`cdn.xn--b6gac.eu.org`、`cdn-all.xn--b6gac.eu.org`、`bestproxy.onecf.eu.org`、`proxyip.cmliussss.net`。
3. 试问面板：`/panel`，部署成功后，在 url 后面增加/panel来进行访问面板，访问面板修改的密码将会保存在`kv`对里。
4. 面板设置要注意：v3.2.0 及以上版本，IP/域名用回车键`ENTER`分隔；v3.1.4 及以下版本，IP/域名用英文逗号`,`分隔。
5. 旧版本升级为新版本（直接新版本的请忽略）的问题：请删除旧的`PROXYIP`变量，建立新的`PROXY_IP`变量后重试部署项目；`/panel`数据会清空，升级前注意备份数据；请在`/panel`面板里点击🔄重置默认值后，才能保存数据。

## IP优选工具的使用
1. win 电脑下载 IP优选工具/[CF优选官方IP[win电脑版].7z](https://github.com/Setout8/Book-Pen-Book/blob/main/IP%E4%BC%98%E9%80%89%E5%B7%A5%E5%85%B7/CF%E4%BC%98%E9%80%89%E5%AE%98%E6%96%B9IP%5Bwin%E7%94%B5%E8%84%91%E7%89%88%5D.7z)，解压后，退出VPN，运行本软件。
2. 下载[CloudflareScanner](https://github.com/bia-pain-bache/Cloudflare-Clean-IP-Scanner/releases/tag/v2.2.5)，解压后，退出VPN，运行本软件。

# 特别感谢
[bia-pain-bache](https://github.com/bia-pain-bache)
