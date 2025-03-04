#Logging into VPS
1. Open terminal 
2. `ssh root@yourvpsipaddress`
3. Enter password


#Common errors 
WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED! 
1. Solution:
`ssh-keygen -R youripaddress`
2. Restart Terminal
3. Re-login

os: ubuntu recommended