After a lot of research on the web, I found it was a pain in the ass to communicate with the RCX on a MacBook Pro running OS X Mavericks.
By now, the only (and best) solution is to use NQC.

NQC is a programming language with a syntax similar to C but it's Not Quite C. 
For more information and documentation:
http://bricxcc.sourceforge.net/nqc/

NQC is provided as a simple command line program which acts as a compiler and a tool to communicate with your RCX hardware to transmit firmware and programs.

Follow these simple steps and you'll be able to enjoy programming your old RCX brick on a modern Intel Mac.
(For the lazy ones, I also provide a compiled version inside the /binaries folder. Copy it inside your /usr/local/bin directory)

The only requirement is a Serial to USB adapter to connect the IR Tower to your computer. 
Find a cheap one based on the PL2303 chip and install the kernel extension: http://www.xbsd.nl/2011/07/pl2303-serial-usb-on-osx-lion.html

(I don't know if NQC works with the USB IR Tower on OS X since I only have the serial version)

Building NQC from sources:

git clone https://github.com/Glitchbone/mindstorms-rcx-osx-tools.git
cd mindstorms-rcx-osx-tools
git submodule init
git submodule update
cd nqc
sudo make install