
1、名词规范
    
- 计算机处理的数据： 数据包
- 物理网卡处理的数据： 数据帧

2、IP地址

网间同行协议地址，用来在网络同行中唯一标识一台主机
    
    IP地址目前有两类：
        IPV4    目前主流    32bit 的整数
        IPV6    未来趋势    128bit 的整数
        
3、IP地址的表示
    
    二进制整数：  11000000 10101000 00000001 00000001
    点分十进制:   192.168.1.1
    十六进制：    0xc0800101
    
            
    IP地址 = 网络地址 +　子网地址　＋　主机地址
    
    主机地址
            全0 表示网段        
            全1 表示广播地址
            其他：标识主机，只有相同网络地址的主机才能直接通信
4、IPV4地址的分类

- A 类：32bit中以0开头的地址，1字节网络地址+3字节主机地址，用来管理超大规模的网络，通常是国家级通信的主干网
 
       
        0.0.0.0 - 127.255.255.255
        10网段是私有IP，用作搭建大型局域网
        127网段是保留地址，用作本地回环

- B 类：32bit中以10开头的地址，2字节网络地址+2字节主机地址，用来管理大规模的网络


        128.0.0.0 - 191.255.255.255
        172.16.xxx.xxx - 172.31.xxx.xxx  私有地址
    
    
- C 类：32bit中以110开头的地址，3字节网络地址+1字节主机地址，用来管理小型的网络

    
        192.0.0.0 - 223.225.255.255
        192.16.xxx.xxx 私有地址
- D 类：32bit中以1110开头的地址。组播地址，不用来表示主机，也不划分网段

        
        224.0.0.0 - 239.255.255.255
        
- E 类：32bit中以11110开头的地址。用作实验、测试，不用做标识主机

        240.0.0.0 - 247.255.255.255
        
5、子网掩码
用来在ABC网段基础下划分子网，子网掩码和IP地址“位与” 后得到网络段号，即“子网掩码 & IP地址 = 网络地址”


    例如：
    11000000 10101000 00000001 00001010              192.168.1.10          IP地址
    11111111 11111111 11111111 00000000              255.255.255.0        子网掩码
    11000000 10101000 00000001 00000000              192.168.1.0            网络段

划分子网分类管理，可以减少网管的负载并预防广播风暴