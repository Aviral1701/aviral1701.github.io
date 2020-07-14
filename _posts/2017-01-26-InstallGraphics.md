---
layout: post
title: Installing graphics.h on your Ubuntu 16.04 
---

Installing graphics.h on your ubuntu os can be a confusing process especially for a beginner.So here are the steps for it: 

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
	initgraph(&gd, &gm, ""); 
  line(100,100,1000,1000) ;
	closegraph();
}
```
## Error Handling: 
+ Some of you might some errors while installing build essential or the other packages.The terminal offers some suggestions at such errors,which you can follow to proceed with your Installations!

<b>Check out my project made using graphics: </b>[View Project](https://github.com/Aviral1701/Lpp-Solver)
<br>
<b>Thanks for reading.Happy `<coding>!`</b>

