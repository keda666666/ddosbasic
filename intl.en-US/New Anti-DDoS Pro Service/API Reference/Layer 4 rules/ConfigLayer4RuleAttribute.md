# ConfigLayer4RuleAttribute {#reference3370 .reference}

You can call this operation to set the attributes of layer 4 forwarding rules, including session persistence and anti-DDoS protection policies.

## Request parameters { .section}

|Name|Type|Required|Description|
|----|----|--------|-----------|
|InstanceId|String|Yes|The ID of the Anti-DDoS Pro instance that you want to change settings for.|
|ForwardProtocol|String|Yes|The forwarding protocol. Valid values:TCP and UDP.|
|FrontendPort|Integer|Yes|The port for front-end connections.|
|Config|String|Yes|The configuration information. You may specify a TcpConfig or UdpConfig object represented as a JSON string. For more information, see [TcpConfig](#) and [UdpConfig](#).|

|Name|Type|Required|Description|
|----|----|--------|-----------|
|PersistenceTimeout|Integer|Yes|The session timeout. Unit: seconds. Default value: 0. A value of 0 indicates that session persistence is disabled.|
|Synproxy|String|Yes|The false sources feature of anti-DDoS protection. Valid values: off and on.|
|NodataConn|String|Yes|The null session connections feature of anti-DDoS protection. Valid values: off and on.|
|Sla|Sla|Yes|The connection limit on destination IPs. For more information, see [Sla](#).|
|Slimit|Slimit|Yes|The connection limit on source IPs. For more information, see [Slimit](#).|
|PayloadLen|PayloadLen|Yes|The limit on the payload size of each packet. For more information, see [PayloadLen](#).|

|Name|Type|Required|Description|
|----|----|--------|-----------|
|PersistenceTimeout|Integer|Yes|The session timeout. Unit: seconds. Default value: 0. A value of 0 indicates that session persistence is disabled.|
|Synproxy|String|Yes|The false sources feature of anti-DDoS protection. Valid values: off and on.|
|NodataConn|String|Yes|The null session connections feature of anti-DDoS protection. Valid values: off and on.|
|Sla|Sla|Yes|The connection limit on destination IPs. For more information, see [Sla](#).|
|Slimit|Slimit|Yes|The connection limit on source IPs. For more information, see [Slimit](#).|
|PayloadLen|PayloadLen|Yes|The limit on the payload size of each packet. For more information, see [PayloadLen](#).|

|Name|Type|Required|Description|
|----|----|--------|-----------|
|Cps|Integer|Yes|The maximum number of new connections per second to a single destination IP and port. Valid values: 100-100,000.|
|Maxconn|Integer|Yes|The maximum number of concurrent connections to a single destination IP and port. Valid values: 1,000-1,000,000.|
|CpsEnable|Integer|No|Indicates whether Cps is enabled. Valid values:-   0: Disabled
-   1 \(Default\): Enabled

|
|MaxconnEnable|Integer|No|Indicates whether Maxconnection is enabled. Valid values:-   0: Disabled
-   1 \(Default\): Enabled

|

|Name|Type|Required|Description|
|----|----|--------|-----------|
|Cps|Integer|Yes|The maximum number of new connections per second from a single source IP. Valid values: 100-100,000.|
|Maxconn|Integer|Yes|The maximum number of concurrent connections from a single source IP. Valid values: 1,000-1,000,000.|
|CpsEnable|Integer|No|Indicates whether Cps is enabled. Valid values:-   0: Disabled
-   1 \(Default\): Enabled

|
|MaxconnEnable|Integer|No|Indicates whether Maxconnection is enabled. Valid values:-   0: Disabled
-   1 \(Default\): Enabled

|

|Name|Type|Required|Description|
|----|----|--------|-----------|
|Min|Integer|Yes|The minimum payload size of a packet.|
|Max|Integer|Yes|The maximum payload size of a packet.|

## Response parameters { .section}

|Name|Type|Description|
|----|----|-----------|
|RequestId|String|The GUID generated by Alibaba Cloud for the request.|

## Examples { .section}

**Sample requests**

```
{
  "InstanceId": "0bcf28g5-d57c-11e7-9bs0-d89d6717dxbc",
  "ForwardProtocol": "tcp",
  "FrontendPort": 80,
  "Config": "{\"PersistenceTimeout\":80,\"Synproxy\":\"off\",\"NodataConn\":\"off\",\"Sla\":{\"Cps\":10,\"Maxconn\":10},\"Slimit\":{\"Cps\":10,\"Maxconn\":30},\"PayloadLen\":{\"Min\":1,\"Max\":2}}"
}

```

**Sample responses**

```
{
  "RequestId": "0bcf28g5-d57c-11e7-9bs0-d89d6717dxbc"
}

```

