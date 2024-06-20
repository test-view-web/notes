从运输层（Transport Layer，也叫传输层）开始，数据才真正进入网络。传输层通过提供Socket相关接口，为应用程序数据**提供数据进出网络的出入口**，并通过不同端口号（Port Number）区分不同的上层应用。

## 4.1 端口号

传输层通过TCP、UDP或SCTP端口号为上层应用提供服务，不同的端口对应不同的应用或服务。

端口号范围1~1023是知名端口，1024~49151是注册端口，49152~65535是私有端口。知名端口分给众所周知的应用，注册端口需要向IANA申请注册才能使用，私有端口类似于私有IP地址，可以不用申请直接使用，在网络中只要不冲突就可以。

所有端口号都是由IANA（Internet Assigned Numbers Authority，互联网号码分配权威）管理，该组织维护一个在线的数据库并随时更新，所有已注册端口号都会在网站上公布，链接地址如下：[https://www.iana.org/assignments/service-](https://link.zhihu.com/?target=https%3A//www.iana.org/assignments/service-names-port-numbers/service-names-port-numbers.xhtml)[names-port-numbers/service-names-port-numbers.xhtml](https://link.zhihu.com/?target=https%3A//www.iana.org/assignments/service-names-port-numbers/service-names-port-numbers.xhtml)。

部分常见的应用协议及对应端口号如表02-01所示。

表02-01 常用协议及端口表

|   |   |   |
|---|---|---|
|Service Name|Port Number|Transport Protocol|
|ftp-data|20|tcp|
|ftp-data|20|udp|
|ftp-data|20|sctp|
|ftp|21|tcp|
|ftp|21|udp|
|ftp|21|sctp|
|ssh|22|tcp|
|ssh|22|udp|
|ssh|22|sctp|
|telnet|23|tcp|
|telnet|23|udp|
|smtp|25|tcp|
|smtp|25|udp|
|dns|53|tcp|
|dns|53|udp|
|bootps|67|tcp|
|bootps|67|udp|
|bootpc|68|tcp|
|bootpc|68|udp|
|tftp|69|tcp|
|tftp|69|udp|
|http|80|tcp|
|http|80|udp|
|http|80|sctp|
|pop2|110|tcp|

