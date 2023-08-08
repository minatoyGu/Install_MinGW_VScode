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

===Termimal controls===

g++ filename.cpp to compile (Default a.exe)

g++ filename.cpp -o output_filename.exe

With static library linked:

g++ -static-libgcc -static-libstdc++ filename.cpp -o filename.exe

.\filename.exe to run

cd Enter a folder ( you can cd file1\subfile2)

cd .. Out

** makefiles need to use: mingw32-make to run / or you may just remame mingw32-make to make in the bin files.

===For Python===

Sure! Here's a step-by-step guide on how to package a Python script as an executable using `pyinstaller`:

Step 1: Install PyInstaller
Make sure you have `pyinstaller` installed on your system. If not, you can install it using `pip` in the terminal or command prompt:

```bash
pip install pyinstaller
```

Step 2: Prepare your Python Script
Ensure your Python script is ready and located in a directory on your computer. For this example, let's assume the script is named `your_script.py`.

Step 3: Open a Terminal/Command Prompt
Open a terminal or command prompt on your computer. This is where you will run the `pyinstaller` command.

Step 4: Navigate to the Script Directory
Use the `cd` command to navigate to the directory where your Python script is located. For example:

```bash
cd /path/to/your/script/directory
```

Step 5: Package the Script as an Executable
Run the following command to package your Python script as an executable:

```bash
pyinstaller --onefile your_script.py
```

This command bundles everything into a single executable file. If you prefer having a folder with the executable and dependencies, omit the `--onefile` option.

Step 6: Find the Generated Executable
After the packaging process is complete, you can find the generated `.exe` file in the `dist` folder within your script directory. This is the standalone executable that you can distribute and run on Windows systems without Python or any other dependencies.

Step 7: Test the Executable
Run the generated `.exe` file to ensure that your program works as expected. It should behave similarly to when you run the Python script directly.

That's it! You've successfully packaged your Python script as an executable using `pyinstaller`. Now you can share the executable with others, and they can run it on their Windows systems without needing Python installed.

Important Note:
If your Python script uses libraries like Selenium, which require additional setup or driver files when running in a headless environment like an executable, make sure to provide the necessary drivers and configurations along with the executable for it to work correctly. Additionally, always test the executable thoroughly before distributing it to ensure all functionalities are working as expected.
