# Redis集群版

通过本文您可以了解云数据库Redis集群版的监控项。

当您调用云监控的API接口时，需要获取当前云产品的**Namespace**和**Period**，具体取值如下：

-   **Namespace**为**acs\_kvstore**。
-   **Period**默认为60秒，也可以为60的整数倍。

当前云产品的**MetricName**和**Dimensions**的取值如下表所示。

|监控项|单位|MetricName|Dimensions|Statistics|
|---|--|----------|----------|----------|
|平均响应时间|us|ShardingAvgRt|userId、instanceId、nodeId|Average、Maximum|
|连接数使用率|%|ShardingConnectionUsage|userId、instanceId、nodeId|Average、Maximum|
|CPU使用率|%|ShardingCpuUsage|userId、instanceId、nodeId|Average、Maximum|
|命中率|%|ShardingHitRate|userId、instanceId、nodeId|Average、Maximum|
|入方向流量|KByte/s|ShardingIntranetIn|userId、instanceId、nodeId|Average、Maximum|
|流入带宽使用率|%|ShardingIntranetInRatio|userId、instanceId、nodeId|Average、Maximum|
|出方向流量|KByte/s|ShardingIntranetOut|userId、instanceId、nodeId|Average、Maximum|
|流出带宽使用率|%|ShardingIntranetOutRatio|userId、instanceId、nodeId|Average、Maximum|
|缓存内Key数量|个|ShardingKeys|userId、instanceId、nodeId|Average、Maximum|
|最大响应时间|us|ShardingMaxRt|userId、instanceId、nodeId|Average、Maximum|
|内存使用率|%|ShardingMemoryUsage|userId、instanceId、nodeId|Average、Maximum|
|QPS使用率|%|ShardingQPSUsage|userId、instanceId、nodeId|Average、Maximum|
|已用连接数|个|ShardingUsedConnection|userId、instanceId、nodeId|Average、Maximum|
|内存使用量|Bytes|ShardingUsedMemory|userId、instanceId、nodeId|Average、Maximum、Sum|
|平均每秒访问次数|个|ShardingUsedQPS|userId、instanceId、nodeId|Average、Maximum|

