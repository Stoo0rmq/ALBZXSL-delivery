# ALBZXSL-delivery

## What is this?
ALBZXSL-delivery consists on a Metasploit Module initially based on the idea of running PowerShell
Scripts on Windows Systems where PowerShell.exe is disabled through Applocker as well as
Windows Script Host. Based on WMIC's XSL script execution policy it loads Empire Framework (https://github.com/EmpireProject/Empire)
on memory using a JS version: Starfighters (https://github.com/Cn33liz/StarFighters)

This crafts an XSL with our PowerShell payload and creates a server which hosts the payload.
### Tell me a bit more about Empire, Starfighters and that stuff.
Empire is a marvelous post-exploitation framework which hundred utilities. It has a PowerShell Windows agent. Which means that you can execute PowerShell scripts where you are not supposed to.

Starfighters is a JS obfuscated version of Empire created by Cn33liz.


## Ok, What are the requirements?
Attacker:
- Metasploit Framework
- Ruby gems:
    - base64
    - socket
    - webrick
Compromised machine: Net Framework 3.5 and PowerShell installed.


##  How am I supposed to install this module?
Put "ALBZXS-delivery.rb" on the following path: ~/.msf4/modules/auxiliary/

## How do I run this module?
Once MSF is loaded:
 1. use auxiliary/windows/albzxml-delivery
 2. set LHOST,LPORT,RESOURCE (full path to .PS1) at least
 3. run the provided command on the compromised machine



## Others
### Why don't you use X instead of Y? / I want to improve it!
Every opinion is welcome! Don't hesitate to contact me or pull a request
### Does this bypasses updated AV's?
No. This method is blocked by AMSI. There are several ways of bypassing AMSI. But still need to learn
how to deal with it. Already workin' on it mate!


#### To-Do
- Create guide of use
- Upload non-dependent MSF ruby script.
- V2 bypass AV
