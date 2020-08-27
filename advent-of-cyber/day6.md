# Day 6

So I am given a holidaytheif.pcap file which I open in wireshark. 

Reading the support material I am notified that there are several Data Exfiltration techniques. Namely:
- DNS
- FTP/SFTP based file transfer
- SMB based file transfer
- HTTP/HTTPS 
- Steganographical methods, like hiding data within images
- ICMP
- And many more. The sky's the limit for Exfiltration methods.

I am notified to look for things that don't seem right to determine malicious traffic. 

I spot a domain and I look know this isn't right.

The document further tells me I am able to export all objects for further analysis.

I am given 3 files:
- Zip file
- Image 
- Webpage

## What data was exfiltrated via DNS?
I found this particular question tough, I wasn't spotting that the domain which I had noticed earlier was actually holding a hex code, which I could then convert back to ascii to reveal a message and thus the answer.

Lesson: Look at what I have and breakdown the bits.

## What did Little Timmy want to be for Christmas?
This was simpler, I had the files I installed fcrackzip and I was able to crack the zip's password and reveal the answer.

## What was hidden within the file?
I installed steghide as instructed but was slightly delayed in understanding that when steghide asked for a passphrase I can just hit enter(_no passphrase given_) and the files would come out. I thought I needed to find the passphrase first. 

Once I hit enter I was then given the file hidden within the image and thus the flag.
