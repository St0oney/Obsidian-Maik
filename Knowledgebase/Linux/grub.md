# Password reset root
> **Beim Hochfahren Shift drücken und dann folgendes im Terminal eingeben**

>sudo fdisk -l

> sudo mkdir /mnt/myroot

> sudo mount /dev/sdXXX /mnt/myroot

> sudo chroot /mnt/myroot

> passwd username

> exit

> sudo unmount /mnt/myroot 

> reboot

