##下单

商户通过该接口将订单同步到车联网

###接口链接

URL地址：

https://iov.service.baidu.com/iovorder/api/generateorder

###请求参数

 |参数名 |类型|是否必填|最大长度|描述|实例值
| :------| :------ | :------ | :------ | :------ | :------ 
 |uid |Bigint|是|-|百度用户id| 149235070
 |identity_no  |String|是| |车联网分配的商户号|10001
 | device_id | String| 是 |32 |设备号||
 | longitude|String | 是 | -|设备当前经度 |116.289573|
 | latitude | String| 是 | -|设备当前纬度|39.9948|
 | car_number | String | 否 |8|车牌号|京Bxxxxx |
 | version | String| 是 |5 |调用的接口版本固定值为1.0||
|out_trade_no |String|是|32|商户订单号|900020199
|goods_name|String|是|128|商品名称，允许包含中文；不超过128个字符或64个汉字 ||
|goods_url|String|是|255|商品在商户网站上的url；不超过255个字符 ||
|goods_unit_price|Int|是|-|商品单价，以分为单位 ||
|goods_count|Int|是|-|商品数量 ||
|goods_total_price|Int|是|-|订单总金额,以分为单位||
|transport_price|Int|是|-|运费，以分为单位||
|out_trade_time|String|是|19|业务订单生成时间,格式为"yyyy-MM-dd HH:mm:ss"|2018-08-08 08:08:08|
|expire_time|String|是|19|交易的过期时间,格式为"yyyy-MM-dd HH:mm:ss"|2018-08-08 08:08:08|
|extra|String|是|500|扩展字段，业务自己决定放什么；不超过500个字符；json格式||
|time |Int|是|10|发送请求的时间戳，精确到秒|1514917884|
|sign |String| 是|-|商户请求参数的签名串，详见签名|详见[签名与验签](/jie-kou-gui-ze/qian-ming.md)|



 ###返回结果

|参数名 |类型|是否必填|最大长度|描述|实例值
| :------| :------ | :------ | :------ | :------ | :------
 |errno|Int|是|-|返回码|0|
 |errmsg|String|是|64|返回信息|| 
 |data |Object |是|-|返回数据||


 data字段为json格式，参数如下：
 
 
|参数名 |类型|是否必填|最大长度|描述|实例值
| :------| :------ | :------ | :------ | :------ | :------
| order_id |String|是|64| 车联网订单id|1069227442364|
 
###请求实例

###响应实例

