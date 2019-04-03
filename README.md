# ac-api

### 设备上报参数设置接口

**request**

```
POST /store/v1/putDevParams

{
	"name": "POWER_TRANS_TAB",
	"type": 7,
	"description": "变压器",
	"params": [{
		"id": 10,
		"name": "voltage",
		"type": "float",
		"description": "电压值",
	}, {
		...
	}]
}
```

参数说明
| 参数 | 类型 | 描述 | 是否必须 |
| -- | -- | -- | -- |
| name | 字符串 | 设备类型名称 | 是 |
|id|字符串|设备类型id|是|
|description|字符串|描述|是|
|params|字符串|参数列表|是|
|params[].id|整形|参数对应的量测点，即前置机上报数据的key值|是|
|params[].name|字符串|参数名称|是|
|params[].type|字符串|参数类型，目前支持int,float,bool,string四种|是|
|params[].description|字符串|参数描述|否|

**response**
统一接口返回码
