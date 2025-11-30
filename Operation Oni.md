## Descripción

Download this disk image, find the key and log into the remote machine.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download disk image](https://artifacts.picoctf.net/c/71/disk.img.gz)
- Remote machine: `ssh -i key_file -p 57632 ctf-player@saturn.picoctf.net`
## Solución

```
kali㉿kali)-[~]
└─$ file disk.img                  
disk.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0xc,223,19), startsector 2048, 204800 sectors; partition 2 : ID=0x83, start-CHS (0xc,223,20), end-CHS (0x1d,81,52), startsector 206848, 264192 sectors
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ mmls disk.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000471039   0000264192   Linux (0x83)
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ fsstat -o 2048 disk.img
FILE SYSTEM INFORMATION
--------------------------------------------

                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ fls -o 2048 disk.img           
d/d 11: lost+found
r/r 12: ldlinux.sys
r/r 13: ldlinux.c32
r/r 15: config-virt
r/r 16: vmlinuz-virt
r/r 17: initramfs-virt
l/l 18: boot
r/r 20: libutil.c32
r/r 19: extlinux.conf
r/r 21: libcom32.c32
r/r 22: mboot.c32
r/r 23: menu.c32
r/r 14: System.map-virt
r/r 24: vesamenu.c32
V/V 25585:      $OrphanFiles
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ fsstat -o 206848 disk.img
FILE SYSTEM INFORMATION
--------------------------------------------

                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ fls -o 206848 disk.img   
d/d 458:        home
d/d 11: lost+found
d/d 12: boot
d/d 13: etc
d/d 79: proc
d/d 80: dev
d/d 81: tmp
d/d 82: lib
d/d 85: var
d/d 94: usr
d/d 104:        bin
d/d 118:        sbin
d/d 464:        media
d/d 468:        mnt
d/d 469:        opt
d/d 470:        root
d/d 471:        run
d/d 473:        srv
d/d 474:        sys
V/V 33049:      $OrphanFiles
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ fls -o 206848 disk.img 470
r/r 2344:       .ash_history
d/d 3916:       .ssh
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ fls -o 206848 disk.img 3916
r/r 2345:       id_ed25519
r/r 2346:       id_ed25519.pub
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ icat -o 206848 disk.img 2345           
-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
QyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLAAAAJgxpYKDMaWC
gwAAAAtzc2gtZWQyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLA
AAAECItu0F8DIjWxTp+KeMDvX1lQwYtUvP2SfSVOfMOChxYGCtd7hso2E7OQItY6aTjMMy
KZb1FVmeBfnVjyHcGYosAAAADnJvb3RAbG9jYWxob3N0AQIDBAUGBw==
-----END OPENSSH PRIVATE KEY-----
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ icat -o 206848 disk.img 2346
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIGCtd7hso2E7OQItY6aTjMMyKZb1FVmeBfnVjyHcGYos root@localhost
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ icat -o 206848 disk.img 2345 > id_ed25519
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ ls
concat_v.png          Desktop   Documents  _dolls.jpg.extracted  id_ed25519  key_file  picker-III.py  picker-I.py  picker-IV.c  Public            Templates  Videos
dds1-alpine.flag.img  disk.img  dolls.jpg  Downloads             index.html  Music     picker-II.py   picker-IV    Pictures     SafeOpener.class  timer.apk
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ ls - l id_ed24519
ls: cannot access '-': No such file or directory
ls: cannot access 'l': No such file or directory
ls: cannot access 'id_ed24519': No such file or directory
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ ls -l id_ed25519 
-rw-rw-r-- 1 kali kali 411 Nov 30 00:20 id_ed25519
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ chmod 600 id_ed25519
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ ls -al          
total 389728

                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ ssh -i id_ed25519 -p 65170 ctf-player@saturn.picoctf.net
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.8.0-1041-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@challenge:~$ ls
flag.txt
ctf-player@challenge:~$ cat flag.txt
picoCTF{k3y_5l3u7h_af277f77}ctf-player@challenge:~$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.

```
## Notas

## Referencias
