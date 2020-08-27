# Day 4

## How many files are visible?
Simple task, but pay attention to the question. `ls -la` shows all hidden files. 

## What is the content of file5?
Simple again, `cat file5`.

## Which file contains the string 'password'?
This is simple enough. I used grep, but maybe better to use strings before grepping.

## What is the IP address in a file in the home folder?
Grep but with a regex for IP address format.

## How many users can log into the machine?
This one was very simple but I opted to try and find a file which would tell me this. 
I was constantly counting `/etc/passwd` file, I should've just changed directory to `cd /home`. 

Important lesson: Think simpler.

## What is the sha1 hash of file8?
Simple enough task, but I mistook the contents of the file as the sha1 hash. 
When in reality the contents is an actual SHA256.

Used `cat file8 | sha1sum`

## What is mcsysadmin's password hash?
Obvious checks is to go to `cat /etc/shadow`. But as expected the file is restricted to root. 
Knowing I don't have root access, I gave up.

I didn't think outside the box to assume maybe there was a backup file.

Lesson: think outside the box more. 
