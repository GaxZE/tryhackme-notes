# Day 2

## What is the path of the hidden page?
Instructed by the support material to use a tool called `DirSearch` this would allow me to brute force check the routes on the website.

I needed to provide a word list for this brute-force approach. 

Results came back that `/sysadmin` was the only path I didn't know of.

Viewing the source code I see a comment:

```html
    <!--
    Admin portal created by arctic digital design - check out our github repo
    -->
```

## What is the password you found?
Based on the comment in the source code. I googled "arctic digital design site:github.com"

There I was able to grab default credentials.

## What do you have to take the 'partay'

Logged in using the credentials and I then saw the last flag.
