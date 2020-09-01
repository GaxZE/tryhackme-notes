# Day 8

Given some information about how we need to escalate a users priviledges. 

Given ip, username and password to ssh into a server.

## What port is SSH running on?

Immediately told that port 22 isn't open, so I need to scan the target ip for all open ports. I do this with nmap and specifcally the `-sS -p-` flags.

## Find and run a file as igor. Read the file /home/igor/flag1.txt

Instructions tell me to look for a SUID bit. This will identify a file which I can run as `igor` and thus allow me to read the flag1.txt file. Using find is instructed. I just need to find out what files/binaries igor can run. Useful flags `-user` & `-group`

## Find another binary file that has the SUID bit set. Using this file, can you become the root user and read the /root/flag2.txt file?

My thought process was lacking here. I had the command to list all binaries with SUID bits set so I can run them as root. My issue was reading the detailed information given to me. Had I noticed that a file was recently edited in comparison to others - I would probably have cracked this one without using hints.

Also worth noting using `file` to establish the files information would benefit me as well.

Once I spotted this, I was able to run the command and get the flag.
