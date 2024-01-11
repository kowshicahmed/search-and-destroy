# Installation
## Easy way
	sudo apt install cmake 					//cmake
	sudo apt  install cmake-curses-gui   	//ccmake

## Installing Latest Version
* go to cmake site
* copy the link for .sh version under linux
* download the sh file using terminal: `curl <link> -o cmake.sh`
* test the sh file using: `sh <filename> --help` `sh <filename> --version`
* install cmake in the current directory in a folder(cmake-test-install)

	`sh cmake-3.21.3-linux-x86_64.sh --prefix=cmake-test-install/ 		//accept(y) two times`
* to install globally we install it in usr/local since it is not managed by system package manager
* we also need to exclude the subdirectory

	`sudo sh cmake-3.21.3-linux-x86_64.sh --prefix=/usr/local/ --exclude-subdir`
* check the version

	`usr/local/bin/cmake --version`


# Running cmake
* to build using cmake
* go to build folder

	`cmake ..`

	`cmake --build .`
* or we can just type, instead of `cmake --build .`

	`make`
* or we can use ccmake to see the gui text editor

	`ccmake ..`
* to use cmake gui

	`cmake-gui`



# Adding libraries
* the default type of library if we dont specify anything is static
* we can change it to shared also 
* using the ldd <executable filename> command we can see the linker dependancy
* we change the type while running cmake also
	`cmake -D BUILD_SHARED_LIBS=TRUE .`
	`make`

# Tutorials
* [CMake-constref-youtube](https://www.youtube.com/playlist?list=PLe51gEr18GGi5sRrgxoXclKjR4tXUz0lZ)
* [Learning CMake Series-youtube](https://www.youtube.com/playlist?list=PL-UNXjSqcu61LEUuH5PIk2VOsnlaVhKju)



