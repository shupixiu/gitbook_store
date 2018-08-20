###商户接入车联网，调用API必须遵循以下规则：
1、传输方式：为保证交易安全性，采用HTTPS传输
2、提交方式：采用POST的提交方式
3、字符编码：统一采用UTF-8字符编码

###公共参数

| 参数 | 类型 | 是否必填|最大长度|描述|实例值
| :------| :------ | :------ | :------ | :------ | :------ 
| car_number | String | 是 | 32| 车辆注册id| |
| longitude|String | 是 | | ||
| latitude | String| 是 | | ||
| app_id | String| 是 | 32|车联网分配给开发者的应用ID|2018081888888|
| timestamp | |  | |发送请求的时间||
| version | String| 是 | |调用的接口版本||






公共请求参数
参数	类型	是否必填	最大长度	描述	示例值
app_id	String	是	32	支付宝分配给开发者的应用ID	2014072300007148
method	String	是	128	接口名称	alipay.trade.fastpay.refund.query
format	String	否	40	仅支持JSON	JSON
charset	String	是	10	请求使用的编码格式，如utf-8,gbk,gb2312等	utf-8
sign_type	String	是	10	商户生成签名字符串所使用的签名算法类型，目前支持RSA2和RSA，推荐使用RSA2	RSA2
sign	String	是	344	商户请求参数的签名串，详见签名	详见示例
timestamp	String	是	19	发送请求的时间，格式"yyyy-MM-dd HH:mm:ss"	2014-07-24 03:07:50
version	String	是	3	调用的接口版本，固定为：1.0	1.0
app_auth_token	String	否	40	详见应用授权概述	
biz_content	String	是		请求参数的集合，最大长度不限，除公共参数外所有请求参数都必须放在这个参数中传递，具体参照各产品快速接入文档	






