# shellshock-scan

The shellshock-scan script from p33kab00 was used as the basis [Github](https://github.com/p33kab00/shellshock-scan)
shellshock-scan is a tiny script that automates the process of identifying and probing [ShellShock](https://www.cvedetails.com/cve/CVE-2014-6271/) vulnerable CGI scripts on Unix web servers. 


Installation
----

You can download shellshock-scan by cloning the [Git](https://github.com/Kostia2004/shellshock-scan3) repository:

    git clone https://github.com/Kostia2004/shellshock-scan3.git

shellshock-scan works out of the box with [Python](http://www.python.org/download/) version **3.7.x** and more on any platform.

Usage
----

Identify and probe CGI scripts w/ approx 250 common scripts:

    $ python shellshock-scan.py http://192.168.5.138
    [*] shellshock-scan3
    [*] by Kostia2004
    [*] # of checks: 225
    
    [+] We've got a candidate: /cgi-bin/status
        Whoa - it's vulnerable!
    
    [*] Found 1 vulnerable scripts in 15901 ms.

Identify and probe CGI scripts on a host w/ a user-defined list of CGI-scripts:

    $ python shellshock-scan.py http://192.168.5.138 cgi-scripts.lst 
    [*] shellshock-scan3
    [*] by Kostia2004
    [*] # of checks: 1357
    
    [+] We've got a candidate: /cgi-bin/status
        Whoa - it's vulnerable!
    
    [*] Found 1 vulnerable scripts in 22623 ms.
