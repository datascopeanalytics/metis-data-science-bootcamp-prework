## Alternative matplotlib installation



This is another way of installing matplotlib and other packages, but
is more likely to run into problems.


### Freetype and png libraries (necessary for matplotlib)

Open a terminal and type the following:

     sudo mkdir -p /usr/local/include
     sudo ln -s /usr/X11/include/freetype2/freetype /usr/local/include/freetype
     sudo ln -s /usr/X11/include/ft2build.h /usr/local/include/ft2build.h
     sudo ln -s /usr/X11/include/png.h /usr/local/include/png.h
     sudo ln -s /usr/X11/include/pngconf.h /usr/local/include/pngconf.h
     sudo ln -s /usr/X11/include/pnglibconf.h /usr/local/include/pnglibconf.h

     sudo mkdir -p /usr/local/lib
     sudo ln -s /usr/X11/lib/libfreetype.dylib /usr/local/lib/libfreetype.dylib
     sudo ln -s /usr/X11/lib/libpng.dylib /usr/local/lib/libpng.dylib

This puts links of these files where matplotlib looks at.
The sudo command will prompt your password.
If you get errors about not finding the files that you are trying to
link to, this means you don't have X11 installed. You can install it
from [here](http://xquartz.macosforge.org/landing/), and then repeat
these steps.


### Pip

Pip is a python package manager. Install it with

     sudo easy_install pip


### iPython, Numpy, Scipy

Now we can use pip to install these packages

     sudo pip install ipython
     sudo pip install numpy
     sudo pip install scipy

### Matplotlib

     sudo pip install matplotlib

Note: With any of these pip packages, if you already have it
installed, add an --upgrade to the end like this:

     sudo pip install matplotlib --upgrade

to make sure you have the latest version.

Also, here are online resources that you can refer to if your setup
hits any unexpected problems:
[A larger stack with virtual environment](http://www.tapir.caltech.edu/~dtsang/python.html)
[Linking X11 method](https://github.com/rueckstiess/mtools/wiki/matplotlib-Installation-Guide)
[Homebrew method](http://penandpants.com/2012/02/24/install-python/)

