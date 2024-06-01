# Nmap

Enumerate all open ports:
```bash
nmap -Pn -p- -oN all_ports.nmap 192.168.178.1
```

Enumerate services on open ports:
```bash
nmap -Pn -p 53,80,139,443,445,5060,5357,8181-8186,45701,49000,49200,49443,55393 -sV -sC -oN services.nmap 192.168.178.1
```

# Podcast creation

Creating a new podcast fires an HTTP request:
![[Pasted image 20240414161225.png]]

I.e. the specified podcast URL is used in a command to request it:
![[Pasted image 20240414161414.png]]

=> TODO: check for cmd execution

# Manual firmware update

Possible through file upload:
![[Pasted image 20240414170715.png]]

=>TODO: Check if we can modify a firmware image

# Save/restore config

Its possible to save the router configuration. A password has to be specified.
![[Pasted image 20240414170830.png]]

Its not possible to save a config file, modify it and restore the modified file. The password is probably used to hash or encrypt parts of the config file.

Note: By modifying some config values, it might be possible to gain command execution.

=> TODO: find out how the password is used and create a valid modified config file