Installing Cython on Windows!
===================
Missing Step By Step Guide
-------------


Simple installation and configuration of **Cython** on Windows can be problematic. Here You will find all steps including MinGW installation, needed to bootstrap Your compiler.


Instruction
-------------

**STEP 1**
Simply install Cython by console: 
> **pip install cython**

**STEP 2**
Install MinGW compiler from [this localization](http://sourceforge.net/projects/mingw/files/latest/download?source=files).  **Do not** install any additional packages right after install. You will do it from console in one of the next steps.

**STEP 3**
Add location of MinGW compiler (for example **c:\mingw\bin**) to Your system path. 
> GO TO: **Control Panel -> System -> Advanced Tab -> Environment Variables -> System Variables**
> Find entry named "**Path**" and add Your path at the end after semicolon

**STEP 4**
Open Windows command line console -> CMD: 
> **mingw-get install gcc**
> **mingw-get install mingw-utils**

**STEP 5**
Go to Python distutils folder (for example **C:\Python34\Lib\distutils**):
Create file named **distutils.cfg** containing:
> **[build]**
> **compiler=mingw32**
