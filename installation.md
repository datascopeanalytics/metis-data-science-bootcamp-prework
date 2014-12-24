## Installing the necessary packages

You will first install some important packages. A lot of this involves
typing commands in the terminal. (In case you haven't used the
terminal in a Mac OS X before, you can open it by holding down
Command, hitting Space, typing terminal, and clicking on the terminal
application that looks like a black box)

### Apple's Xcode and Command Line Tools

Xcode is the developer's suite for OSX that comes free from Apple,
however, it doesn't come installed by default. Command Line Tools is a
part of it that makes the OS X command line behave more like
Unix. Since OSX Lion, the Xcode installation doesn't include the
command Line Tools by default.

###### On Mac OS X Lion / Mountain Lion
You can install Xcode via the
[App Store](https://itunes.apple.com/us/app/xcode/id497799835).

Once Xcode has been installed, run Xcode and then open the
preferences. Select the Download section and the Components tab and
install Command Line Tools from there.

###### On Mavericks / Yosemite
You can install Command Line Tools directly on a terminal with

    xcode-select --install

### Homebrew

Homebrew is an excellent package manager for OSX. If you don't have
it, install it with

     ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
     
Open the .bash_profile file in your home directory (create one if it
doesn't exist) and add this line:

     export PATH=/usr/local/bin:/usr/local/share/python:$PATH

Homebrew installs packages in /usr/local/ and this makes sure you can
run these packages from the command line.
To apply this change, do

     source ~/.bash_profile

Or alternatively, close the terminal and open a new one.

### Python

We will use homebrew to install python. OS X comes with python, but
it's runtime environment is not up to date. Install python with

     brew install python

This may take a while. Now when you do

     which python

you should see

     /usr/local/bin/python

### Pip

Pip is a python package manager. Install it with

     easy_install pip

### Numpy and Scipy

Numpy and Scipy are the fundamental scientific computing packages for python.
Use pip to install them:

     pip install numpy
     pip install scipy

NOTE: If you encounter an error in either of these steps, try installing gfortran (a dependency) with homebrew:

     brew install gfortran
     
and then try again. Gfortran comes with gcc, already provided by OS X, but older versions did not have it.

### iPython and iPython notebook

     pip install ipython[notebook]

### Statsmodels

     pip install statsmodels

### Matplotlib

     brew install pkg-config
     pip install matplotlib


###### Note
With any of these pip packages, if you already have it
installed, add an --upgrade to the end like this:

     pip install matplotlib --upgrade

to make sure you have the latest version.


### Test that you have the right environment

Type

     ipython

to open an ipython IDE. Then test numpy, scipy and matplotlib:

     import numpy
	 import scipy
	 import statsmodels
	 import matplotlib

There shouldn't be any errors.

If for some reason you don't want to use homebrew, or you hit
unexpected problems, you can check out the [alternative installation
guide](alternative_installation.md) to reach this step.

### Scikit.learn

Scikit.learn is an excellent machine learning library for python.

     pip install scikit-learn

### Pandas is a data analysis library for python.

     pip install pandas


### Test scikit-learn and pandas

Open up the python interpreter with

     python

and try importing these packages

     import sklearn
	 import pandas

There should be no errors.

### Git

Git is a version control tool. You can use the graphical installer
that you can download from
[here](http://sourceforge.net/projects/git-osx-installer/).

Congratulations! You are done with installing packages!
