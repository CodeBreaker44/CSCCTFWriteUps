# CSCCTFWriteUps

#Reset my VM!!

First thing when you boot up the image of the machine you will need to enter a password for the user like this:

![image](https://user-images.githubusercontent.com/89404773/211173893-03de046d-4988-4080-94fa-b6c35e79dce7.png)



of course, you won’t be able to gain access to it so just like the name of the challenge you need to reset the VM password

to do that first reset the VM to access the boot up menu for the machine:

![image](https://user-images.githubusercontent.com/89404773/211173946-21e95245-ac28-4e54-8ac0-115e67e58988.png)

then while the machine is booting up press and hold the ``` shift ``` button, after that you will be promoted to the following screen:

![image](https://user-images.githubusercontent.com/89404773/211173982-3dbdaac4-13d2-4994-832e-5a8795b72ee9.png)

With the list of options available, hit the e key.

An editor like this will show:

![image](https://user-images.githubusercontent.com/89404773/211174042-e4562765-2a96-42ff-89b7-fdf3652fb419.png)

keep going down until you see a line similar to this 

``` linux /boot/vmlinux-3.13...-generic root=UUID=<uuid> ro ```

At the end of it add ``` single ``` .

* The idea is to enter ``` single user ``` mode so it be possible to rest the VM password

after adding ```single``` to the line mentioned earlier it will look something like this:

![image](https://user-images.githubusercontent.com/89404773/211174131-d16f0958-d9fb-4438-9074-2d076153fe74.png)

hit ``` ctrl + x ``` to continue

you will be presented with a console and the root prompt (#): use the passwd command to change your user's password:

``` # passwd user ```

![image](https://user-images.githubusercontent.com/89404773/211174172-454990fb-813e-4c8d-ab0e-8eb1232d8856.png)

hit ``` CTRL + d ``` to reboot the machine

enter the new password you created, the machine will be unlocked and the flag will be the wallpaper of the machine:

![image](https://user-images.githubusercontent.com/89404773/211174221-8255721d-8498-4f4b-8344-1f46cfbaeeb2.png)

FLAG: CSCCTF{f0r3n51c5_g0d_n1ce_j0b!!}
