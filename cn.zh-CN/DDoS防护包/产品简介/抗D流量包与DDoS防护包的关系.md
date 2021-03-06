# 抗D流量包与DDoS防护包的关系 {#concept_68482_zh .concept}

如果您的DDoS防护包需要具备弹性防护能力，您可以通过购买抗D流量包来抵扣您的DDoS防护包所产生的弹性防护流量费用。

**说明：** 购买DDoS防护包时，您将获得包含一定流量的抗D流量包供您免费使用（购买专业版防护包实例赠送2 TB弹性防护流量；企业版防护包实例赠送30 TB弹性防护流量）。因此，您可以安心为您的DDoS防护包开启弹性防护功能。

DDoS防护包的实际费用包含两部分：

|费用|说明|
|--|--|
|保底防护带宽费用|根据您所购买的DDoS防护包规格，一次性支付DDoS防护包的保底带宽费用。|
|弹性防护流量费用|不同类型的DDoS防护包的计费方式有所不同。 -   **专业版**：根据实际使用中超出保底防护带宽所产生的弹性防护流量进行计费。
-   **企业版**：根据实例全部入方向流量计算弹性防护流量费用。

 需要通过您额外购买的抗D流量包，抵扣DDoS防护包实际产生的弹性防护流量。|

## 弹性防护流量计算示例 {#section_1tj_mx5_p3b .section}

-   **专业版**：例如，您选购的专业版DDoS防护包的规格是“20G保底防护带宽+100G弹性防护带宽”。在一个弹性防护流量计费周期（五分钟）内，该DDoS防护包防御了10秒钟50Gbps的流量攻击，则该流量攻击产生的弹性防护总流量为37.5GB = 10\[秒，攻击持续时间\] \* （50\[Gbps，实际攻击流量\]-20\[Gbps，保底防护带宽\]）/8\[单位转换\]。因此，在该弹性防护流量计费周期内，您的抗D流量包需要被扣除37.5GB的流量。

    **说明：** 低于保底带宽的流量不计入弹性防护流量。

-   **企业版**：例如，您选购的是企业版DDoS防护包。在一个弹性防护流量计费周期（五分钟）内，该DDoS防护包入方向的带宽为100Mbps（无论是否遭受攻击），则该计费周期内的弹性防护总流量为3.75GB = 300\[秒，计费周期\] \* 0.1\[Gbps，入方向带宽\] \* /8\[单位转换\]。因此，在该弹性防护流量计费周期内，您的抗D流量包需要被扣除3.75GB的流量。

同时，您可以在[云盾DDoS防护管理控制台](https://yundunnext.console.aliyun.com/?p=ddosbgp)中的**流量包**页签，查看该计费周期内所抵扣的弹性防护流量。

