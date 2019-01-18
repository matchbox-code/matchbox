Additional preperation for Windows and Mac OS:

Windows:
Download the latest version of Cygwin from http://www.cygwin.com. View full list of packages. 
Search for ‘make’ and ‘vim’ packages and install them. Installed packages should have status ‘Keep’ instead of ‘Skip’. 
By default, the installer does not install these packages. The installer can be used to add packages to the existing installation.
Mac:
Install llvm with brew. In Makefile.gnu_32: Change all g++ to clang++.
Remove –lrt flags. Get version number of llvm: llvm-config –-version
Create a link for libomp.dylib: 
cd /usr/local/lib
ln -s /usr/local/Cellar/llvm/<version number>/lib/libomp.dylib libomp.dylib

To compile:

go to the matchbox root directory and run "make" for the debug version or "make optimized" for the optimized one.

To run:

Go to examples/debug or examples/optimized and run an executable file without arguments you will see what the arguments need to be. 
For example run ./BptMaxCard. 

Input: 

-The graph file must be in mtx format and for non-bipartite algorithm the mtx file must be symmetric. 
-Vertex weights flie must be in the following format:
n
w(v1)
w(v2)
.
.
w(vn)
Where n is number of vertices and w(vi) is the weight of ith vertex.