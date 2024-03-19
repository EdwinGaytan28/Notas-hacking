## Objetivo
We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.
## Solución
```
──(kali㉿kali)-[~]
└─$ wget https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery     
--2024-03-19 15:29:22--  https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 202940 (198K) [application/octet-stream]
Saving to: ‘mystery.1’

mystery.1           100%[================>] 198.18K  73.7KB/s    in 2.7s    

2024-03-19 15:29:25 (73.7 KB/s) - ‘mystery.1’ saved [202940/202940]

                                                                             
┌──(kali㉿kali)-[~]
└─$ file mystery     
mystery: data
                                                                             
┌──(kali㉿kali)-[~]
└─$ hexeditor mystery

zsh: suspended  hexeditor mystery
                                                                             
┌──(kali㉿kali)-[~]
└─$ hexeditor mystery
                                                                             
┌──(kali㉿kali)-[~]
└─$ hexeditor mystery
                                                                             
┌──(kali㉿kali)-[~]
└─$ sudo apt install pngcheck
[sudo] password for kali: 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
E: Unable to locate package pngcheck
                                                                             
┌──(kali㉿kali)-[~]
└─$ sudo apt install pngcheck
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
E: Unable to locate package pngcheck
                                                                             
┌──(kali㉿kali)-[~]
└─$ sudo apt install pngcheck
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
E: Unable to locate package pngcheck
                                                                             
┌──(kali㉿kali)-[~]
└─$ 
                                                                             
┌──(kali㉿kali)-[~]
└─$ sudo apt update          
Get:1 http://kali.download/kali kali-rolling InRelease [41.5 kB]
Get:2 http://kali.download/kali kali-rolling/main amd64 Packages [19.6 MB]
Get:3 http://kali.download/kali kali-rolling/main amd64 Contents (deb) [46.7 MB]
Get:4 http://kali.download/kali kali-rolling/contrib amd64 Packages [116 kB]
Get:5 http://kali.download/kali kali-rolling/contrib amd64 Contents (deb) [245 kB]
Get:6 http://kali.download/kali kali-rolling/non-free amd64 Packages [193 kB]
Get:7 http://kali.download/kali kali-rolling/non-free amd64 Contents (deb) [892 kB]
Get:8 http://kali.download/kali kali-rolling/non-free-firmware amd64 Packages [33.1 kB]
Get:9 http://kali.download/kali kali-rolling/non-free-firmware amd64 Contents (deb) [16.8 kB]
Fetched 67.8 MB in 1min 51s (610 kB/s)                                      
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
453 packages can be upgraded. Run 'apt list --upgradable' to see them.
                                                                             
┌──(kali㉿kali)-[~]
└─$ sudo apt install pngcheck
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following NEW packages will be installed:
  pngcheck
0 upgraded, 1 newly installed, 0 to remove and 453 not upgraded.
Need to get 68.6 kB of archives.
After this operation, 208 kB of additional disk space will be used.
Get:1 http://kali.download/kali kali-rolling/main amd64 pngcheck amd64 3.0.3-3 [68.6 kB]
Fetched 68.6 kB in 1s (61.8 kB/s) 
Selecting previously unselected package pngcheck.
(Reading database ... 404048 files and directories currently installed.)
Preparing to unpack .../pngcheck_3.0.3-3_amd64.deb ...
Unpacking pngcheck (3.0.3-3) ...
Setting up pngcheck (3.0.3-3) ...
Processing triggers for man-db (2.12.0-3) ...
Processing triggers for kali-menu (2023.4.7) ...
                                                                             
┌──(kali㉿kali)-[~]
└─$ pngcheck -v mystery
zlib warning:  different version (expected 1.2.13, using 1.3)

File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 2852132389x5669 pixels/meter
  CRC error in chunk pHYs (computed 38d82c82, expected 495224f0)
ERRORS DETECTED in mystery
                                                                             
┌──(kali㉿kali)-[~]
└─$ hexeditor mystery        
                                                                             
┌──(kali㉿kali)-[~]
└─$ pngcheck -v mystery
zlib warning:  different version (expected 1.2.13, using 1.3)

File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
:  invalid chunk length (too large)
ERRORS DETECTED in mystery
                                                                             
┌──(kali㉿kali)-[~]
└─$ hexeditor mystery  
                                                                             
┌──(kali㉿kali)-[~]
└─$ pngcheck -v mystery
zlib warning:  different version (expected 1.2.13, using 1.3)

File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
:  invalid chunk length (too large)
ERRORS DETECTED in mystery
                                                                             
┌──(kali㉿kali)-[~]
└─$ hexeditor mystery  
                                                                             
┌──(kali㉿kali)-[~]
└─$ pngcheck -v mystery
zlib warning:  different version (expected 1.2.13, using 1.3)

File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
  chunk IDAT at offset 0x00057, length 65445
    zlib: deflated, 32K window, fast compression
  chunk IDAT at offset 0x10008, length 65524
  chunk IDAT at offset 0x20008, length 65524
  chunk IDAT at offset 0x30008, length 6304
  chunk IEND at offset 0x318b4, length 0
No errors detected in mystery (9 chunks, 96.3% compression).
                                                                             
┌──(kali㉿kali)-[~]
└─$ open mystery
                                                                             
┌──(kali㉿kali)-[~]
└─$ 


picoCTF{c0rrupt10n_1847995}
```
## Notas adicionales

## Referencias

