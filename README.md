# Opennero install instructions
This instruction mainly focuses on linux users. 

If you are MAC users, follow steps on Opennero wiki https://github.com/nnrg/opennero/wiki, it should work. If not, use GDC public machines. 

If you are Windows users, try to install the OpenNERO yourself(we don't support windows installation), or use GDC public machines.

## Install instructions (Your own machine with root privileges)
1 run the following commands:

    git clone https://github.com/Grem-Lin/Opennero.git
    cd Opennero
    chmod +x setup.sh
    sudo setup.sh
  Note: if your linux is 18.04, you need to install python-wxgtk 3.0 instead of python-wxgtk2.8 as shown in setup.sh
2 Download the corresponding linux version of binary file for Opennero:

 Ubuntu 14.04: https://drive.google.com/open?id=1sOjh7FapZA6RjmJCHDV4qZhsx9YtmD9X
 
 Ubuntu 16.04: https://drive.google.com/open?id=1b-ayq6zC_bXqvTw0LQSEwyWvynVAC-kV
 
 Ubuntu 18.04: https://drive.google.com/open?id=16jl3jzGHdvHLzOC7qUhnG42zgFEnQzZJ

3 unzip the file and run: 

    cd ./dist 
    ./OpenNERO

## Install instructions (GDC public machine without root privileges)
There are 3 approaches:
### Go to GDC public lab and directly use public machines(RECOMMENDED):

1 Download 18.04 version of binary file and unzip

2 $ cd dist

3 $ ./OpenNERO

### Using GDC machine remotely with ssh:

(Note: you need to figure out how to set up ssh if your machine is not connected with internet or wifi in GDC. You can refer to 
https://www.cs.utexas.edu/facilities-documentation/ssh-keys-cs-mac-and-linux )

0 Setup ssh -X 
 - adding '+iglx' to file /usr/share/lightdm/lightdm.conf.d/50-xserver-command.conf as follows:    
    
    [SeatDefaults] 
    
    \# Dump core
    
    xserver-command=X -core +iglx
 - Ctrl-Alt-F1 and relogin
 - $ sudo service lightdm restart
 
1 ssh -X username@hostname.cs.utexas.edu (username: your cs account, hostname: CS host name, you can refer to  https://apps.cs.utexas.edu/unixlabstatus/ to find available host name  )

2 Download 18.04 version of binary file and copy file into username@hostname.cs.utexas.edu:~

3 $ cd dist

4 $ ./OpenNERO

### Using GDC machine remotely with xpra:
Learn it by yourself with following steps:

- install xpra on your local machine
- "cshosts publinux" to find a list of linux hosts you can xpra to
- ssh eg. to "sorry.cs.utexas.edu"
- start xpra on sorry
    xpra start :100 --start-child=xterm
- start xpra on your local machine
  mode ssh
  user@sorry.cs.utexas.edu 22 100
  type user's password
  connect
  type ssh passphrase
- cd to opennero directory
- setenv LD_LIBRARY_PATH /u/risto/bin/boost_1_54_0/stage/lib/:/lusr/share/software/matlab-r2018b/bin/glnxa64
- ./OpenNERO
- after done:
  if multiple xpras run at the same time it won't work, so stop it with
    xpra stop :100


