# Day 7

I am given a large bit of reading material all about the fundamentals of networking.

This information is worth re-reading.

Good information about setting up and enumerating the target.

Nmap flags:
```
-sT is a TCP connect scan(which is the same as the 3 way handshake). It uses this to check if the port is open
-sS is a TCP stealth scan which only sends one packet to see if the TCP port is open
-p port-number is used to specify what port to scan:
-p- can also be used to scan all the ports
-F is a common flag used to specify the top 250 common ports
-O is used to determine the host operating system
-sC is used to run default scripts. NMAP has particular scripts it can run against services running on hosts to gain more information
-sV is used to determine the versions of services running on open ports
-T is used to specify the timing with 1 being the slowest and 5 being the fastest. The faster the scan, the more unreliable the results. A good compromise is 3
```

## How many TCP ports under 1000 are open?
In order to achieve this, I need to scan all TCP ports within the range of 1-1000. 
This was done with: `-p 1-1000` as the flag.

## What is the name of the OS of the host?
Interestingly no exact matches of the OS was found on my nmap scan. But it did print out "aggressive OS guesses" of which Linux was 91%. But when running the port scan on `-p 1-1000` I was able to notice the OS.

## What version of SSH is running? 	
Nmap printed these results.

## What is the name of the file that is accessible on the server you found running?
The ports open was 999,22,111. Noticing the port 999 was running a SimpleHTTPServer.. I decided to visit this in my browser. Upon visiting the ip:999 I was able to see the file and it's name.
