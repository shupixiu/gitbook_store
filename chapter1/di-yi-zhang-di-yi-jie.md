

| 参数 | 类型 | 是否必填|最大长度|描述|实例值
| :------| :------ | :------ | :------ | :------ | :------ 
| car_number | String | 否 |8|车牌号|京Bxxxxx |
| longitude|String | 是 | |经度 |116.289573|
| latitude | String| 是 | |纬度|39.9948|
| app_id | String| 是 | 32|车联网分配给开发者的应用ID|2018081888888|
| timestamp | |  | |发送请求的时间||
| version | String| 是 |5 |调用的接口版本固定值为1.0||
| device_id | String| 是 |32 |设备号||





##alipay.trade.fastpay.refund.query(统一收单交易退款查询)
###接口链接

URL地址：https://iov.service.baidu.com/iovorder/api/generateorder

###请求参数
 |参数名 |类型|是否必填|最大长度|描述|实例值
| :------| :------ | :------ | :------ | :------ | :------ 
 |uid |Bigint|是|-|百度用户id| 149235070
 |out_trade_no |String|是|32|商户订单号|900020199
 |identity_no  |String|是| |车联网分配的商户号|10001
 | device_id | String| 是 |32 |设备号||
 | longitude|String | 是 | -|设备当前经度 |116.289573|
 | latitude | String| 是 | -|设备当前纬度|39.9948|
 | car_number | String | 否 |8|车牌号|京Bxxxxx |
 | version | String| 是 |5 |调用的接口版本固定值为1.0||
 |time |Int|是|-|发送请求的时间戳，精确到秒|
 |sign |string| 是|商户请求参数的签名串，详见签名|详见示例
|goods_name|String|是|128|商品名称，允许包含中文；不超过128个字符或64个汉字 ||
|goods_url|String|是|255|商品在商户网站上的url；不超过255个字符 ||
|goods_unit_price|Int|是|-|商品单价，以分为单位 ||
|goods_count|Int|是|-|商品数量 ||
|goods_total_price|Int|是|-|订单总金额,以分为单位||
|transport_price|Int|是|-|运费，以分为单位||
|out_trade_time|String|是|19|业务订单生成时间,格式为"yyyy-MM-dd HH:mm:ss"|2018-08-08 08:08:08
|expire_time|String|是|19|交易的过期时间,格式为"yyyy-MM-dd HH:mm:ss"|2018-08-08 08:08:08
|extra|String|是|500|扩展字段，业务自己决定放什么；不超过500个字符；json格式|


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
 
 
 
 




##alipay.trade.fastpay.refund.query(统一收单交易退款查询)
商户可使用该接口查询自已通过alipay.trade.refund提交的退款请求是否执行成功。 该接口的返回码10000，仅代表本次查询操作成功，不代表退款成功。如果该接口返回了查询数据，则代表退款成功，如果没有查询到则代表未退款成功，可以调用退款接口进行重试。重试时请务必保证退款请求号一致。
###公共参数
###请求地址
| 左对齐标题 | 右对齐标题 | 居中对齐标题 
| :------| ------: | :------: 
| 短文本 | 中等文本 | 稍微长一点的文本 
| 短文本 | 中等文本 | 稍微长一点的文本 



