# Day 1

## What is the name of the cookie used for authentication?
Create an account use dummy data. 
Login with credentials. 
Open browsers inspector and inspect the cookie.

## If you decode the cookie, what is the value of the fixed part of the cookie?
Decoding the cookie, it looked like `base64` encoding so I simply used this to decode: `echo <cookie> | base64 --decode`.

Key part of the question is then 'the fixed part'.

I noticed it was in a format: `<myusername>v4er9ll1!ss`


## After accessing his account, what did the user mcinvetory request?
To access his account I needed to swap the `username` in the cookie and refresh the browser.
