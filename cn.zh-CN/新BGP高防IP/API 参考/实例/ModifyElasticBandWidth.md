# ModifyElasticBandWidth {#reference553 .reference}

调用ModifyElasticBandWidth修改指定实例的弹性防护带宽。

## 请求参数 { .section}

|名称|类型|是否必需|描述|
|--|--|----|--|
|InstanceId|String|是|要操作的实例ID。单次请求只支持修改1个实例的弹性防护带宽，且目标实例必须是正常状态。|
|ElasticBandwidth|Integer|是|新的弹性带宽值。|

## 返回参数 { .section}

|名称|类型|描述|
|--|--|--|
|RequestId|String|本次请求的ID。|

## 示例 { .section}

**请求示例**

```
{
  "InstanceId": "0bcf28g5-d57c-11e7-9bs0-d89d6717dxbc",
  "ElasticBandwidth": 50
}

```

**返回示例**

```
{
  "RequestId": "0bcf28g5-d57c-11e7-9bs0-d89d6717dxbc"
}

```

