# Day 3

## Whats the destination IP on packet number 998?
We was given a pcap file. The support material suggested opening it with Wireshark. 
The packet number 998 was the key packet we had to investigate.

Wireshark gives the IP address of the packet 998.

## What item is on the Christmas list?
Inspecting the packet and after "following the TCP stream" option in Wireshark I was able to see the contents of the packet.

At the top of the file it explained the "christmas list" entry.

## Crack buddy's password!
Also in the TCP stream, was the users password hash.

The support documentation suggested looking at https://hashcat.net/wiki/doku.php?id=example_hashes to see what hash the password matched.

The key bit is the `$6` in the hash, this lead me to `1800` hash-mode.
_Tip_: `hashcat -h | grep \$6` would've achieved same result.

I was then instructed to use the application `hashcat` and pop the hash into a file for bruteforcing.

I also needed the rockyou.txt wordlist to brutefoce the password.

```console
hashcat -m 1800 password.txt rockyou.txt --force
```
