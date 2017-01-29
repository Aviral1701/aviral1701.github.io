
Alot of you might have tried installing graphics.h on your ubuntu system,but must be having a hard time.So here are the steps for installing graphics.h library on your Ubuntu 16.04 and latter.

## Steps:
+ Download Graphics Package for Ubuntu here: [Libgraph](http://download.savannah.gnu.org/releases/libgraph)
<br>
+ Install build essential: `sudo apt-get install build-essential`
<br>
+ Install Packages: <br>
`sudo apt-get install libsdl-image1.2 libsdl-image1.2-dev guile-1.8 guile-1.8-dev libsdl1.2debian libart-2.0-dev libaudiofile-dev libesd0-dev libdirectfb-dev libdirectfb-extra libfreetype6-dev libxext-dev x11proto-xext-dev libfreetype6 libaa1 libaa1-dev libslang2-dev libasound2 libasound2-dev`
<br>
+ Extract the file and copy the contents into your USR directory: `sudo cp -r libgraph-1.0.2 /usr/local/lib`
<br>
+ Compile C++ file with: `gcc test.c -lgraph`

## Code Sample:
```C++
#include<graphics.h>

int main()
{
	int gd = DETECT, gm;
	initgraph(&gd, &gm, ""); //in Windows instead of Null you have to provide path of graphic drivers!
  line(100,100,1000,1000) ;
	closegraph();
}
```
## Error Handling: 
+ Some of you might some errors while installing build essential or the other packages.The terminal offers some suggestions at such errors,which you can follow to proceed with your Installations!
<hr>
<b>Thanks for reading.Happy `<coding>!`<b>
<hr>
