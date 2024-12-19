# DYNAMIC_NATMEDENCE

## static NAT (__nem nem a nemzeti alaptanterv...__)


```bash
R2(config)# ip nat inside source static 192.168.10.254 209.165.201.5

R2(config)# interface serial 0/1/0
R2(config-if)# ip address 192.168.1.2 255.255.255.252
R2(config-if)# ip nat inside
R2(config-if)# exit
R2(config)# interface serial 0/1/1
R2(config-if)# ip address 209.165.200.1 255.255.255.252
R2(config-if)# ip nat outside
```
__DONE__

## check commandok:

R2# show ip nat translations
R2# show ip nat translations
R2# show ip nat statistics
R2# show ip nat translation verbose
R2# clear ip nat translation *
R2# show ip nat translation

# GOATED golden grep | kereső commandok

R2# show running-config | include NAT
R2# show running-config | include anyu_es_apu_testverek_uwu
R2# show running-config | include pool
R2# show running-config | include ip address


# Dynamic NAT (goated)

R2(config)# ip nat pool NAT-POOL1 209.165.200.226 209.165.200.240 netmask 255.255.255.224
R2(config)# access-list 1 permit 192.168.0.0 0.0.255.255
R2(config)# ip nat inside source list 1 pool NAT-POOL1

R2(config)# interface serial 0/1/0
R2(config-if)# ip nat inside
R2(config)# interface serial 0/1/1
R2(config-if)# ip nat outside

