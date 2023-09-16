First what we need to do is check what's happend on the server, and what kind of port are open, let's turn on the nmap, here's the results:

![obraz](https://github.com/Anogota/Wifinetic/assets/143951834/dd06067d-410f-4b64-8151-d22407304a47)

That how can see, we can log in into as anonymous on FTP, and on on the previous screan scan, you can see some directorys and file.
We can download, but how can see on this scan, there is smothing intresting backup-OpenWrt-2023-07-26.tar, get this file on your desktop, and untar this file by this command: tar -xvf backup-OpenWrt-2023-07-26.tar, we got a /etc go into this directory, first what i recoomand is use: grep -iR password, but i don't have any results, i did some recon and in /etc/config found wireless, there we can see password

![obraz](https://github.com/Anogota/Wifinetic/assets/143951834/8a5841fd-65d5-48ff-ba3a-8036482ade44)

And also i found /etc/passwd there we can find some users.
We can see there one intresting user, netadmin

![obraz](https://github.com/Anogota/Wifinetic/assets/143951834/fd6b0fc4-abbc-4740-b7f2-eee51aa7539e)

