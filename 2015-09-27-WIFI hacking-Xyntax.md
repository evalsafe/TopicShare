#WiFi Hacking  
##设备  
- 外接无线网卡 淘宝：8187L  
- kali linux  

##登入  

### WPA/WPA2  
  - 抓握手包,暴力破解：aircrack-ng minidwep-gtk  
  - 半握手包破解https://github.com/dxa4481/WPA2-HalfHandshake-Crack/  

### WEP  
 - 直接搞定  

###密码破解  

####online crack  
 - http://www.onlinehashcrack.com  
 - http://wpa.darkircop.org/index.php  
 - http://free.wpapass.com/auth/signup  

###漏洞&后门  
 - routerpwn  


----------


##后续攻击  

###ARP欺骗  

####解析原理  

```flow  
op=>operation: MAC:F0-76-1C-BA-8B-93  
op1=>operation: Host IP:192.168.1.1  
op2=>operation: Domain:www.baidu.com  
op2->op1->op  
```  

####ARP过程  

```sequence  
AP->C1:who has 192.168.1.101  
C1-->AP:.101 的MAC地址是 A  
AP-C1:数据发送到MAC A  
```  

####欺骗过程  

```sequence  
AP->C1:who has 192.168.1.101  
AP->Hacker:who has 192.168.1.101  
C1-->AP:.101 的MAC地址是 A  
Hacker-->AP:.101 的MAC地址是 B  
AP->Hacker:数据发送到MAC B  
Hacker->C1:处理过的数据  
```  

 - 修改数据（替换图片 网页代码注入）  
 - 替换下载（绑马）  

###DNS欺骗 dns spoof  
 - 挂相似网页做钓鱼  
 - 工具：dns_spoof(ettercap 已集成)  

###deauth  
 - wifijammer  
 - python scapy  
 - wifi杀手    

###嗅探   
 - 明文密码  
 - SSL证书伪造  
 - SSLstrip（ettercap sslstrip）  

###会话劫持 session hijacking  
 - Cookies  
 - 工具：ferret+hamster  

----------


##Fake AP  
 - wifiphisher（kali1可直接使用）  
 - 重定向或者本地服务器挂钓鱼网页  
 - iw ifconfig iwconfig iptables hostapd  
![Fake AP](http://img.blog.csdn.net/20151018165127379)  


----------

##zANTI  
 - android  
 - dsploit/csploit  

![zANTI](http://img.blog.csdn.net/20151018130916983)  


----------


##防御  

 - IP MAC 绑定  
 - 黑/白名单  
