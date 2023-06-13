---

title: Cisco NAT Translation # change the title
author: EightBitOni
date: 2023-06-10 00:00:00 -0600 # year, month, day
categories: [Cisco,Routing]
tags: [cisco,routing] # all lower case
pin: false

---

## simple nat

create ip nat inside with private IP

```shell
interface FastEthernet0  
ip address 10.0.0.1 255.255.0.0
ip nat inside  
```

create ip nat outside public ip
```
interface FastEthernet1  
ip address 174.143.212.1 255.255.252.0  
ip nat outside
```

