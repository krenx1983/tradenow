## **CTP接口兼容模拟交易平台（支持Windows、Linux、MacOS、FreeBSD）**

CTP接口兼容模拟交易平台，采用与CTPAPI完全兼容的接口，一定程度上可替代simnow等模拟平台进行功能测试。 CTP程序无需修改代码也无需重新编译，只需在这里**下载与CTP API版本号一致的交易dll**，覆盖掉自己的即可，**行情dll不用改**，行情的接入地址可使用各期货公司的实盘地址。

目前已提供CTPAPI全部在用的四个版本API，提供**Win32、Win64、Linux64、Mac64及FreeBSD64**共5个平台40个动态库。

### 支持负价交易（合约号MINUS为负价合约，价格为负数，每手保证金为固定金额）

### 撮合方式（同时支持做市与仿真）：
- 仿真：完全由用户之间撮合，按价格优先、时间优先撮合成交。仿真模式的合约有三个，分别为TEST、BTC、MINUS，其它合约均为做市模式。
- 做市：Simnow用的就是做市模式，以实盘行情盘口做市撮合成交，即高于叫卖价的多单立即成交，低于叫买价的空单立即成交，否则挂在队列中等行情符合条件的时候成交。

### **交易前置地址：**

- tcp://121.36.146.182:20002

### **行情前置地址：** （随便找的几个实盘地址，自己可以替换成其它的，行情前置都是不校验密码的，用户名也可以为空）

- tcp://180.169.112.54:42213
- tcp://140.207.168.9:42213
- tcp://180.168.212.75:41313
- tcp://27.115.78.155:41313
- tcp://180.168.102.233:41168
- tcp://112.64.143.220:41168

### **模拟账号：** （以下模拟账号的密码均为123456，初始资金为10000000）

- 90001
- 90002
- 90003
- 90004
- 90005
- 90006
- 90007
- 90008
- 90009

### **QQ技术交流群：**

![QQ群二维码](https://user-images.githubusercontent.com/83346523/123681604-99a1e380-d87c-11eb-9ac1-301551cc704c.jpg)

### **特别说明：**

AuthCode、AppID认证信息任意填，不作校验

Broker任意填，填什么就回什么

<u>tradenow行情前置地址：tcp://121.36.146.182:20004，虽然也可以从tradenow接收实时行情，但是不建议这么做，除非玩TEST等自建合约，否则建议直接使用CTP数据源。从tradenow接收行情，同交易一样需要更换行情dll。</u>

### **可以关注公众号了解更多信息：**
![qrcode_for_gh_564e4bf4668c_258](https://user-images.githubusercontent.com/83346523/120095274-ad600a00-c157-11eb-8496-7d680bd1f39b.jpg)

**本平台为个人自建平台，希望大家手下留情，不要给太大的压力。**

<u>*本模拟平台没有像simnow那样严格遵循各交易所规则，如：不计持仓明细，因此平仓不存在先开先平等规则，只是对总持仓进行处理。如有较高测试要求的请连simnow或联系期货公司。*</u>
<u>*本模拟平台不对模拟结果作任何保证，依据本平台测试结果进行实盘交易的后果完全由使用者自己承担。*</u>
