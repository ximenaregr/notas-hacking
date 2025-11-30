## Descripción

Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)

Additional details will be available after launching your challenge instance.
## Solución

```      
┌──(kali㉿kali)-[~]
└─$ file disk*                     
disk.flag.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0xc,223,19), startsector 2048, 204800 sectors; partition 2 : ID=0x82, start-CHS (0xc,223,20), end-CHS (0x16,111,25), startsector 206848, 153600 sectors; partition 3 : ID=0x83, start-CHS (0x16,111,26), end-CHS (0x26,62,24), startsector 360448, 253952 sectors
disk.img:      DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0xc,223,19), startsector 2048, 204800 sectors; partition 2 : ID=0x83, start-CHS (0xc,223,20), end-CHS (0x1d,81,52), startsector 206848, 264192 sectors
disk.img.gz:   gzip compressed data, was "disk.img", last modified: Tue Sep 21 19:34:53 2021, from Unix, original size modulo 2^32 104857600
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~]
└─$ gzip -d disk.img.gz    
gzip: disk.img already exists; do you wish to overwrite (y or n)? y
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~]
└─$ ls
concat_v.png          Desktop        disk.img   dolls.jpg             Downloads  flag.txt.enc  index.html  Music          picker-II.py  picker-IV    Pictures  SafeOpener.class  timer.apk
dds1-alpine.flag.img  disk.flag.img  Documents  _dolls.jpg.extracted  flag.txt   id_ed25519    key_file    picker-III.py  picker-I.py   picker-IV.c  Public    Templates         Videos
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~]
└─$ mmls disk.img     
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)
                                                                                                                                                                                                                                           

┌──(kali㉿kali)-[~]
└─$ nc saturn.picoctf.net 54953
What is the size of the Linux partition in the given disk image?
Length in sectors: 202752
202752
Great work!
picoCTF{mm15_f7w!}
```
## Notas

## Referencias
