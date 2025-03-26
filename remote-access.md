To gain access to the TARGET remote machine, we have to create the malware which will grant our ATTACKER machine access to exploit processes on the TARGET machine.

To craft the malware, we make use of the MSFvenom commands.

**MSFvenom** is a penetration testing tool used to create payload for exploitation and post-exploitation.

we make use of the help page of MSFvenom to craft a proper malware
```
msfvenom -h
```
To list out multiple payloads on the MSFvenom page, we use the command 
```
msfvenom -l payloads
```
