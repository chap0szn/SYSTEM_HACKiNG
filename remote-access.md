To gain access to the TARGET remote machine, we have to create the malware which will grant our ATTACKER machine access to exploit processes on the TARGET machine.

To craft the malware, we make use of the MSFvenom commands.

**MSFvenom** is a penetration testing tool used to create payload for exploitation and post-exploitation.

we make use of the help page of MSFvenom to craft a proper malware
```
msfvenom -h
```
A proper malware has 4 parts; Payload , Platform, Encoder & File format

To list out multiple payloads, platform, encoders on the MSFvenom page, we use the command 
```
msfvenom -l payloads
```
```
msfvenom -l platforms
```
```
msfvenom -l encoders
```


the formula for crafting the basic malware i
