# LFS_remaster

# not complete yet


remastering tools for lfs based os 

 created by purnomo hadi fb:purnomo.shinigami 
 purnomo.shinigami@gmail.com , under GPLv2 or later license 
 this tools only build for remastering LFS based OS
 with AUFS and squashfs tools , initramfs based on linux live kit 
 
 dependencies 
 
-  libisoburn
   
-  squashfs-tools
   
-  sudo
   
-  wget
   
-  git
   
-  xterm
 
 optional dependencies  
 
 -  dialog
 
 you must compile a kernel with aufs patch visit
 https://github.com/sfjro/aufs4-linux/blob/aufs4.x-rcN/Documentation/admin-guide/README.rst

initramfs 
     
compare between linux live script & kolomonggo-init
     
Author of linux live kit : Tomas M <http://www.linux-live.org/>
     
Author of kolomonggo init: purnomo hadi <purnomo.shinigami@gmail.com>
     
initswitch beetwen systemd and sysvinit only for kolomonggo linux system hyrarki 



 
# HOW to use it 
extract to "/" file system don't extrack to other directory and run with root account. and 
create directory sources under "/" example  = /sources
run  
# ./lfskit --built-initrd
 
