   # Extracting Python Source Code from PyInstaller

This repository documents the process to extract Python bytecode (`.pyc` files) from executables created with PyInstaller and recover the original Python source code (`.py`). This method uses the script `pyinstxtractor.py` to extract the compiled files and the online tool [pylingual](https://pylingual.io/) to decompile them.

## Steps to Extract and Recover Python Code

1. Copy the PyInstaller executable (`example.exe`) and the script `decompile.py` into the same folder.

2. Open a Command Prompt in that folder:
   - In Windows, right-click in the folder’s empty space while holding Shift.
   - Select “Open PowerShell window here” or “Open Terminal here”.
   - Alternatively, click on the folder's address bar, type `cmd`, and press Enter.

3. In the terminal window, execute the extraction script using the following command:
   Replace `example.exe` with the actual name of your executable file

 4. Run this command: `python decompile.py example.exe`

5. After execution, a new folder named `example.exe_extracted` will be created automatically in the same directory.

6. Inside the extracted folder, locate the `.pyc` file(s). These files are compiled Python bytecode.

7. To recover the original Python source code:
- Open your browser and go to [pylingual](https://pylingual.io/).
- Upload the extracted `.pyc` file.
- The website will decompile the file and display the recovered Python code.
- Copy or download the resulting `.py` file as needed.

## Notes

- It is recommended to use the same Python version that was used to compile the executable when running `pyinstxtractor.py` to avoid possible extraction errors.
- The script `pyinstxtractor.py` only extracts `.pyc` files; it does not perform decompilation.
- If preferred, local decompilers like `uncompyle6` or `decompyle3` can be used instead of pylingual.io to decompile `.pyc` files.

## Disclaimer

This process is intended exclusively for educational purposes, recovery of your own applications, or analysis in legal contexts. Do not attempt to decompile proprietary or unauthorized software. Always respect software licenses and intellectual property rights.

## Tools Used

- pyinstxtractor.py : https://github.com/extremecoders-re/pyinstxtractor
- pylingual.io : https://pylingual.io/
