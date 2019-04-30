# DescribeLayer4Rules {#reference1674 .reference}

You can call this operation to perform queries on layer 4 forwarding rules of Anti-DDoS Pro instances.

## Request parameters { .section}

|Name|Type|Required|Description|
|----|----|--------|-----------|
|InstanceId|String|Yes|The ID of the Anti-DDoS Pro instance that you want to query.|
|ForwardProtocol|String|No|The forwarding protocol. Valid value: TCP.|
|FrontendPort|Integer|No|The port for front-end connections.|
|Offset|Integer|Yes|The number of records to skip when returning the result records.**Note:** If not specified, all result records are returned.

|
|PageSize|Integer|Yes|The number of result records per page. Maximum value: 50.|

## Response parameters {#section_s32_11v_jgb .section}

|Name|Type|Description|
|----|----|-----------|
|Total|Integer|The total number of result records.|
|Listeners|Listener\[\]|The array of listeners. For more information, see [Listener](#).|
|RequestId|String|The GUID generated by Alibaba Cloud for the request.|

|Name|Type|Description|
|----|----|-----------|
|InstanceId|String|The ID of the Anti-DDoS Pro instance.|
|Protocol|String|The listener protocol.|
|FrontendPort|Integer|The port for front-end \(client to Anti-DDoS Pro\) connections. Valid values: 0-65535.|
|BackendPort|Integer|The port for back-end \(Anti-DDoS Pro to origin server\) connections. Valid values: 0-65535.|
|RealServers|JSON array|The IP addresses of the origin servers.|
|IsAutoCreate|Boolean|Indicates whether the listener is automatically created. If true, the listener cannot be deleted or modified.|

## Examples { .section}

**Sample requests**

```
{
  "InstanceId": "0bcf28g5-d57c-11e7-9bs0-d89d6717dxbc",
  "ForwardProtocol": "tcp",
  "FrontendPort": 80,
  "Offset": 1,
  "PageSize": 10
}

```

**Sample responses**

```
{
  "Total": 1,
  "Listeners": [
    {
      "InstanceId": "0bcf28g5-d57c-11e7-9bs0-d89d6717dxbc",
      "Protocol": "tcp",
      "FrontendPort": 80,
	  "BackendPort":80,
      "RealServers": [
        "1.1.1.1",
        "2.2.2.2"
      ],
      "IsAutoCreate": true
    }
  ],
  "RequestId": "0bcf28g5-d57c-11e7-9bs0-d89d6717dxbc"
}

```
