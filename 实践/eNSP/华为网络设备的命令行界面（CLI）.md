要从用户视图进入系统视图，
```
system-view
```
对于 `int` 或 `interface` 命令，需要指定接口的类型和编号。例如，要配置GigabitEthernet接口0/0/0，您应该使用：
```
interface GigabitEthernet 0/0/0

```

在设置IP地址时，您需要确保命令格式正确。正确的格式是 `ip address [IP地址] [子网掩码]`。例如，如果您想设置IP地址为192.168.1.254，子网掩码为255.255.255.0（等同于/24），您应该输入：
```
ip address 192.168.1.254 255.255.255.0

```
**退出保存**： 配置完成后，退出接口配置模式，保存配置
```
quit
save
```


```
display ip interface brief
```


```
动态NAT ensp实验
Please press enter to start cmd line!

<Huawei>
Jan  7 2024 23:23:19-08:00 Huawei %%01IFPDT/4/IF_STATE(l)[0]:Interface GigabitEt
hernet0/0/0 has turned into UP state.
<Huawei>system-view
Enter system view, return user view with Ctrl+Z.
[Huawei]interface GigabitEthernet 0/0/0
[Huawei-GigabitEthernet0/0/0]display ip interface brief
*down: administratively down
^down: standby
(l): loopback
(s): spoofing
The number of interface that is UP in Physical is 2
The number of interface that is DOWN in Physical is 2
The number of interface that is UP in Protocol is 1
The number of interface that is DOWN in Protocol is 3

Interface                         IP Address/Mask      Physical   Protocol  
GigabitEthernet0/0/0              unassigned           up         down      
GigabitEthernet0/0/1              unassigned           down       down      
GigabitEthernet0/0/2              unassigned           down       down      
NULL0                             unassigned           up         up(s)     
[Huawei-GigabitEthernet0/0/0]
Jan  7 2024 23:23:49-08:00 Huawei %%01IFPDT/4/IF_STATE(l)[1]:Interface GigabitEt
hernet0/0/1 has turned into UP state.
[Huawei-GigabitEthernet0/0/0]display ip interface brief
*down: administratively down
^down: standby
(l): loopback
(s): spoofing
The number of interface that is UP in Physical is 3
The number of interface that is DOWN in Physical is 1
The number of interface that is UP in Protocol is 1
The number of interface that is DOWN in Protocol is 3

Interface                         IP Address/Mask      Physical   Protocol  
GigabitEthernet0/0/0              unassigned           up         down      
GigabitEthernet0/0/1              unassigned           up         down      
GigabitEthernet0/0/2              unassigned           down       down      
NULL0                             unassigned           up         up(s)     
[Huawei-GigabitEthernet0/0/0]ip address 192.168.1.254 255.255.255.0
Jan  7 2024 23:25:26-08:00 Huawei %%01IFNET/4/LINK_STATE(l)[2]:The line protocol
 IP on the interface GigabitEthernet0/0/0 has entered the UP state. 
[Huawei-GigabitEthernet0/0/0]quit
[Huawei]interface GigabitEthernet 0/0/1
[Huawei-GigabitEthernet0/0/1]ip address 10.10.1.1 255.255.255.0
Jan  7 2024 23:25:56-08:00 Huawei %%01IFNET/4/LINK_STATE(l)[3]:The line protocol
 IP on the interface GigabitEthernet0/0/1 has entered the UP state. 
[Huawei-GigabitEthernet0/0/1]quit
[Huawei]display ip interface brief
*down: administratively down
^down: standby
(l): loopback
(s): spoofing
The number of interface that is UP in Physical is 3
The number of interface that is DOWN in Physical is 1
The number of interface that is UP in Protocol is 3
The number of interface that is DOWN in Protocol is 1

Interface                         IP Address/Mask      Physical   Protocol  
GigabitEthernet0/0/0              192.168.1.254/24     up         up        
GigabitEthernet0/0/1              10.10.1.1/24         up         up        
GigabitEthernet0/0/2              unassigned           down       down      
NULL0                             unassigned           up         up(s)     
[Huawei]interface GigabitEthernet 0/0/0
[Huawei-GigabitEthernet0/0/0]quit
[Huawei]interface GigabitEthernet 0/0/1
[Huawei-GigabitEthernet0/0/1]nat staic global 172.16.1.1
                                 ^
Error: Unrecognized command found at '^' position.
[Huawei-GigabitEthernet0/0/1]nat static global 172.16.1.1
                                                          ^
Error:Incomplete command found at '^' position.
[Huawei-GigabitEthernet0/0/1]nat static global 172.16.1.1 inside 192.168.1.1
[Huawei-GigabitEthernet0/0/1]undo nat static global 172.16.1.1 inside 192.168.1.
1
[Huawei-GigabitEthernet0/0/1]nat address-group 1 172.16.1.1 172.16.1.5
[Huawei]acl
            ^
Error:Incomplete command found at '^' position.
[Huawei]acl 2000
[Huawei-acl-basic-2000]rule 5 permit source 192.168.1.0 0.0.0.255
[Huawei-acl-basic-2000]quit
[Huawei]interface GigabitEthernet 0/0/1
[Huawei-GigabitEthernet0/0/1]nat outbound 2000 address-group 1 no-pat
[Huawei-GigabitEthernet0/0/1]
```