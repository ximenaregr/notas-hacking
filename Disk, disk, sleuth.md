## Descripción

Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/2f998eee12730cf5766624681212a441/dds1-alpine.flag.img.gz)
## Solución

```
(kali㉿kali)-[~]
└─$ wget 
                                                                           
┌──(kali㉿kali)-[~]
└─$ gzip -d dds*.gz
                                                                           
┌──(kali㉿kali)-[~]
└─$ file *.img                       
dds1-alpine.flag.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0x10,81,1), startsector 2048, 260096 sectors
                                                                           
┌──(kali㉿kali)-[~]
└─$ strings *.img | grep pico              
ffffffff81399ccf t pirq_pico_get
ffffffff81399cee t pirq_pico_set
ffffffff820adb46 t pico_router_probe
  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_267e38f6}

```
## Notas

## Referencias
