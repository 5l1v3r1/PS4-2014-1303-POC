CVE 2014-1303 Proof Of Concept for PS4
==============
This repository contains a poc for the CVE 2014-1303 originally disclosed by Liang Chen. It has been tested to work on system firmware 2.03, but should work for systems on a firmware < 2.50, the ROP test will however only work on 2.03.

Usage
==============
You need to edit the dns.conf to point to the ip address of your machine, and modify your consoles dns settings to point to it as well. Then run  
`python fakedns.py -c dns.conf`  
then  
`python server.py`  
Debug output will come from this process.  

Navigate to the User's Guide page on the PS4 and various information should be printed to the console. The ROP test will print what is stored in the rsp register. Continuing execution after rsp is pivoted still needs to be done.

Acknowledgements
================
Liang Chen  
thexyz  
dreadlyei
