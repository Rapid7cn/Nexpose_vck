# 欢迎使用Nexpose_vck
本项目本意是为Nexpose/InsightVM产品新增不被其内置的漏洞检测项，以满足广大客户需要，本项目为本人共享，无任何利益驱动。
## Nexpose/InsightVM
Nexpose/InsightVM是Rapid7的漏洞风险管理产品，Rapid7是一家很著名的安全公司，甚至其Metasploit产品比公司名本身更为出名。

Nexpose/InsightVM本身的规则引擎使用的是[jess](https://jessrules.com)，至于如何创建自定义检测项，官方已经有说明，详见<https://kb.help.rapid7.com/docs/nexpose-common-vulnerability-check-examples>。
## 使用方法
Nexpose（InsightVM）本身支持的自定义检测项的目录位置为"/opt/rapid7/nexpose/plugins/java/1/CustomScanner/1/"，自定义的vck和xml文件则要放至此目录。
## 自定义检测项生效方法
需要至产品管理的WEB界面中的管理功能中，进入安全控制台命令行，运行命令"load content"，等待产品定义库重新加载，并留意产品安装目录下的日志目录([INSTALL_DIR]/nexpose/nsc/logs/nsc.log)，查看相关日志，如果正常，则日志条目如下：
2020-04-18T08:59:43 [INFO] Inserted 2 vulnerabilities
2020-04-18T08:59:55 [INFO] Load Content command complete
## 更新
本人工作之余会新增发现的（产品本身未更新）检测项。
诸位如有需要，也可以提交自己的检测项或者需求。
## 记录
* 2020-04-22:更新cve-2020-4276.xml和cve-2020-4362.xml中的severity值（修复值为整数，不然加载报错）。
