# OpenCV Build Script
With this simple bash script, you will *not* need anymore to compile your OpenCV code with the aux of CMakeList & Makefile,
avoiding the stress of compiling copy-pasted code everytime into your config file.

### Pre-requisites
Just Open-CV installed. Depending on what system you run on, you should do the following steps.<br

## Installation
#### -Ubuntu/Debian
 You can fetch the *working* script install [here](https://github.com/milq/milq/blob/master/scripts/bash/install-opencv.sh) if a <b>Ubuntu/Debian</b> user<br>
#### -Arch-Like
 If using an <b>Arch-Like</b> system, just follow those steps:

```console
sudo pacman -S opencv
sudo pacman -S hdf5 vtk
sudo pacman -S glew
```

## Setting the script
# Ubuntu-like Systems
Simple as it is, bebfore using this script is *strongly* suggested to create an alias to make the script executable everywhere<br>
into your system.Instead, it is <b>requested</b> the presence of the OpenCV build dir into the path variables.<br>

If you *don't have* the OpenCV_DIR set into your shell file, you should do something like this (example for *bash shell*, <br>
assuming you have installed OpenCV and it is currently into your main folder): <br>

```console
foo@bar:~$ echo "export OpenCV_DIR=~/your/path/to/OpenCV/build" >> .<<yourshell>rc>
```
example with various shells, if your OpenCV dir is into the *home folder* (~/OpenCV)

1. ZSH
```console
foo@bar:~$ echo "export OpenCV_DIR=~/OpenCV/build" >> .zshrc
```
2. BASH
```console
foo@bar:~$ echo "export OpenCV_DIR=~/OpenCV/build" >> .bashrc
```

# Arch Linux-like Systems
If you got an Arch-like enviroinment (Manjaro, Antegros or Arch) you can just install openCV from<br>
the pre-requisites tutorial or the AUR repo.<br>
In this case, you don't need to set the OPENCV_DIR because the library are installed<br>
into your /usr/lib path.<br>
Just donwload the appropriate BASH script (*build_arch*), rename it to *build* and follow the steps ahead.<br>

# Common Steps

Once done that, create an hidden folder to contain the OpenCV build file: <br>

```console
foo@bar:~$ mkdir ~/.buildOpenCV
```

And copy the <b>build</b> file into this newly folder, i.e. from terminal:

```console
foo@bar:~$ mv /path/to/build ~/.buildOpenCV
```

Once done that, it's almost finished: Just add this line to your shell config file: <br>

1. Bash
```console
foo@bar:~$ echo "alias opencv=~/.buildOpenCV/build" >> .bashrc
```
2. ZSH
```console
foo@bar:~$ echo "alias opencv=~/.buildOpenCV/build" >> .zshrc
```

And now you can just type<br>

```console
foo@bar:~$ opencv OpenCVFile.cpp 
```

To build, compile and link your OpenCV cpp file, avoiding the use of CMakeList. <br>

*obviously* don't forget to <b>run your program!</b> The output of the script will be the name of the input file<br>
 *minus* the *.cpp* extension.
 
 ```console
example: OpenCVTest.cpp -> OpenCVTest
```
  


