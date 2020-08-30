# Day 7

I am given a large bit of reading material all about the fundamentals of networking.

This information is worth re-reading.

Good information about setting up and enumerating the target.

## How many TCP ports under 1000 are open?
In order to achieve this, I need to scan all TCP ports within the range of 1-1000. 
This was done with: `-p 1-1000` as the flag.

## What is the name of the OS of the host?
Interestingly no exact matches of the OS was found on my nmap scan. But it did print out "aggressive OS guesses" of which Linux was 91%. But when running the port scan on `-p 1-1000` I was able to notice the OS.

## What version of SSH is running? 	
Nmap printed these results.

## What is the name of the file that is accessible on the server you found running?
The ports open was 999,22,111. After visiting the ip:999 I was able to see the file and it's name.
