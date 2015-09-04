# zabbix-templates

There is an Mikrotik template. 
I'm checking: traffic on all ports, cpu load, cpu temp, motherboard temp, memory load.
It uses 1 discovery (for ifaces), and 50 items (in initial release, 36 CPUs :)) and 42 static triggers 

Each discovery goes to fill 6 items (port status, port admin status, bytes in, bytes out, pps in, pps out), 
taking via OID (no need to get mib)

Template builded to monitor an Mikrotik CCR1036-8G-2S+, but should fit any other.

For import you need to add regex

<pre>Name: Mikrotik interfaces
Expression: .*slave.*
Result: Result is FALSE
</pre>
