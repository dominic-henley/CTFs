# Information

*Files can always be changed in a secret way. Can you find the flag?*

This challenge comes with a picture:

![cat](https://user-images.githubusercontent.com/80395298/126905702-889a0a78-f353-4504-b11c-4bc0109427cb.jpg)

*How adorable!*

At first I thought this was a steganography challenge, but after investigating I didn't find anything of note. So I tried running `cat cat.jpg` (it is, after all, the name of the challenge).

![image](https://user-images.githubusercontent.com/80395298/126905866-8dbbdfec-bab0-4814-b378-873a8c341c85.png)

*No luck...*

Perhaps checking the hex register?

![image](https://user-images.githubusercontent.com/80395298/126905873-f02114d0-789d-4f70-9660-5d604aae6ccb.png)

Well, we seem to be getting somewhere at least. There seems to be some base64 stuff in the data. 

`cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9` seems to be interesting, looks like it could be the flag.

running `echo cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9 | base64 -d` does indeed result in the flag.

`flag:picoCTF{the_m3tadata_1s_modified}`
