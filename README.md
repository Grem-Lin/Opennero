# Opennero installation instructions

## 1. Linux users installation instructions (You need to have root privileges)
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

## 2. MAC users installation instructions
If you are MAC users, follow steps on Opennero wiki https://github.com/nnrg/opennero/wiki, it should work. If not, use xpra (follow instructions for windows)

## 3. Windows users installation instructions (Using Xpra)
OpenNERO only support linux and Mac system and it has graphics interface. You cannot only use ssh in Windows to run the OpenNERO remotely and thus you need to use xpra instead. Xpra is an open-source multi-platform persistent remote display server and client for forwarding applications and desktop screens. It works for Linux, MAC and Windows. You can find more details here: http://xpra.org/

Please follow this tutorial to setup xpra and Opennero on Windows: https://docs.google.com/document/d/1Xxijp4Sehcsk5jA_i6nPAVpATz5xMIwREkeNqP9pX_I/edit?usp=sharing

Note that this Windows tutorial is also suitable for Linux and Mac users, but the foregoing instructions in first 2 sections are much more easier. 

## 4. Installation instructions for those who can physically access to GDC public machines (currently not available due to COVID-19)

1 Download 18.04 version of binary file  https://drive.google.com/open?id=16jl3jzGHdvHLzOC7qUhnG42zgFEnQzZJ and unzip

    cd dist
    ./OpenNERO


