# IP TABLES RULES ----

## Block all types of access to 'firewall' from 149.154.161.221 network 
```
iptables -t filter -A INPUT -s 149.154.161.221 -j DROP
```

## Check all rules 
```
iptables -L -n
```

## fluss/delete all rules---
```
iptables -F 
```

## Delete the specific rule -
```
iptables -t filter -D INPUT -s 149.154.161.221 -j DROP 
```

## Block all types of access to 'filewall' from any ip we are not able to access anything on 'firewall'. 
```
iptables -t filter -A INPUT -j DROP 
```

# Block Ports ---
### (input direction, telnet/ssh/web services)

## block web access on 'firewall', we are not able to access 'web server on 'firewall'.
```
iptables -t filter -A INPUT -m tcp/udp -p tcp/udp -a 172.24.0.11 --drop 80 -j DROP
```

## we want to block 'telnet'(23) and 'ssh'(22). we could write 2 rules for blocking 2 ports as we did in case of web server but here we will be using 'multiport' module for specifying multiple ports in single rule.
```
iptables -t filter -A INPUT  -m multiport -p tcp/upd -s 172.24.0.11 --dports 22,23 -j DROP 
```
```
iptables -A INPUT -p tcp --dport 22 -j REJECT
```

block 'ssh' and 'telnet'. if we have written incourect rule syntax,'iptables' will show the error	 

### iptables Syntax and Options.
1. -A, --append : Append a rule to a chain.
2. -C, --check	: Look for a rule that matches a chain.
3. -D, --delete : Remove a rule from  a chain.
4. -F, --flush : Remove all rules.
5. -I, --insert : Add a rule to a chain at the provided position.
6. -L, --list : Show all rules in a chain.
7. -N, --new-chain : Create a new chain.
8. -V, --verbose : Show a more details output. 
9. -X --delete-chain : Delete chain.

## Save Rules.
```
iptables-save |sudo tee /etc/iptables/rules.v4
```
(save the rules in 'input-rules-1' file. the file name could be anything)

```
cat input-rules-1
```
(view the save rules)  
but if we reboot system, so rules will gwt lost and we have to restore from 'input-rules-1'file.
1. if to make rules permanent ,we have to save these rules in `/etc/sysconfig/iptables`file.

 

















 
