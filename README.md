# Installing MinGW with Vscode in Windows 11
Here is the method for installing C++ compliers to VScode after the official installer was broken:

1. Download VScode.
2. Install C/C++ extensions in VScode marketplace.
3. Go here: https://www.mingw-w64.org/downloads/
4. Select WinLibs.com version
5. Select UCRT 64 version and download the file (Alawys choose x86*64 if you are using modern windows)
6. Extract it.
7. Put it in the "Program Files" directory.
8. Search for "Edit environment variables"
9. In the "Use variables for [username]", choose "path" -> Edit
10. Add your path (Ends with [...\mingw64\bin])
11. Go cmd, type "g++ --version" to check if you have sucessfully installed.
===Termimal controls====
g++ filename.cpp to compile (Default a.exe)
g++ filename.cpp -o output_filename.exe
.\filename.exe to run
cd Enter a folder ( you can cd file1\subfile2)
cd .. Out
** makefiles need to use: mingw32-make to run / or you may just remame mingw32-make to make in the bin files.
