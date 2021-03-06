# DescribeInstanceStatistics {#reference999 .reference}

You can call this operation to perform queries on the rules configured on instances.

## Request parameters { .section}

|Name|Type|Required|Description|
|----|----|--------|-----------|
|InstanceIds|String|Yes|The array of IDs of Anti-DDoS Pro instances represented as a JSON string.|

## Response parameters { .section}

|Name|Type|Description|
|----|----|-----------|
|InstanceStatistics|InstanceStatistic|The details of the rules on Anti-DDoS Pro instances. For more information, see [InstanceStatistic](#).|
|RequestId|String|The GUID generated by Alibaba Cloud for the request.|

|Name|Type|Description|
|----|----|-----------|
|InstanceId|String|The ID of the Anti-DDoS Pro instance.|
|PortUsage|Integer|The number of layer 4 forwarding rules configured on the instance.|
|DomainUsage|Integer|The number of layer 7 forwarding rules configured on the instance.|

## Examples { .section}

**Sample requests**

```
{
  "InstanceIds": "[\"0bcf28g5-d57c-11e7-9bs0-d89d6717dxbc\",\"0bcf28g5-d57c-11e7-9bs0-d89d6717dxbc\"]"
}

```

**Sample responses**

```
{
  "InstanceStatistics": [
    {
      "InstanceId": "0bcf28g5-d57c-11e7-9bs0-d89d6717dxbc",
      "PortUsage": 20,
      "DomainUsage": 10
    }
  ],
  "RequestId": "0bcf28g5-d57c-11e7-9bs0-d89d6717dxbc"
}

```

