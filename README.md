First what we need to do is check what's happend on the server, and what kind of port are open, let's turn on the nmap, here's the results:

![obraz](https://github.com/Anogota/Wifinetic/assets/143951834/dd06067d-410f-4b64-8151-d22407304a47)

That how can see, we can log in into as anonymous on FTP, and on on the previous screan scan, you can see some directorys and file.
We can download, but how can see on this scan, there is smothing intresting backup-OpenWrt-2023-07-26.tar, get this file on your desktop, and untar this file by this command: tar -xvf backup-OpenWrt-2023-07-26.tar, we got a /etc go into this directory, first what i recoomand is use: grep -iR password, but i don't have any results, i did some recon and in /etc/config found wireless, there we can see password

![obraz](https://github.com/Anogota/Wifinetic/assets/143951834/8a5841fd-65d5-48ff-ba3a-8036482ade44)

And also i found /etc/passwd there we can find some users.
We can see there one intresting user, netadmin

![obraz](https://github.com/Anogota/Wifinetic/assets/143951834/fd6b0fc4-abbc-4740-b7f2-eee51aa7539e)

And if you rember scan, one 22 are open this is a SSH, i tryed log in as: netadmin VeRyUniUqWiFIPasswrd1! 
That how i think, we can login with this creds in SSH.

![obraz](https://github.com/Anogota/Wifinetic/assets/143951834/6b5318d5-5384-442f-b344-b33758d07aa2)

There is a flag, that was pretty easy, to get a user.txt 
I did some recon, but can't find anything intresting, but when i check ps -ef

![obraz](https://github.com/Anogota/Wifinetic/assets/143951834/cdda928e-3fd9-4b61-96bd-de97fc445ebe)

We need to look at the wireless interface configuration with iwconfig. Monitor mode is used for sniffing traffic.

![obraz](https://github.com/Anogota/Wifinetic/assets/143951834/e13c9468-503e-4e3b-ac2b-01df845009c6)

There is interface is being used for monitoring mon0
And i go to google and search something about it. i found something intresting tool reaver

![obraz](https://github.com/Anogota/Wifinetic/assets/143951834/31a550e9-b7dd-4c50-92d7-613e5097e4f9)


![obraz](https://github.com/Anogota/Wifinetic/assets/143951834/de6659ee-59fb-433b-87e1-c3dd416fd8e5)
