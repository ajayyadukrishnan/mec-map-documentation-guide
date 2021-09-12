
# MEC Map Documentation Guide
Guide to use the MEC Map Documentation tool

## Pre-requisites

- MEC Map Documentation Tool
- Notepad++
- MEC Map Current Source File
- Resource Files containing the logo, headers, footers, and the cover page.

## Instructions

1. Get the current source from the MEC and save it as a ***.java*** file
2. Open the ***.java*** file in Notepad++ and run the following  steps to remove unnecessary text. Press **Ctrl + H** to open the Find and Replace window. Select **Regular expression** Radio box and **. matches newline** checkbox
```
Find:

((?:(?:public&#124;private&#124;protected&#124;static&#124;final&#124;abstract&#124;synchronized&#124;volatile)\s+)*)\s*(void&#124;String)\s*(clearIn&#124;clearOut&#124;printOutput&#124;printInput&#124;getErrorMsg)\(.*?\)\s*({(?:{[^{}]*}&#124;.)*?})

Replace:
```
```
Find:

((?:(?:public&#124;private&#124;protected&#124;static&#124;final&#124;abstract&#124;synchronized&#124;volatile)\s+)*)\s*(\w+)\s*\(String ID, String fPath\)\s*({(?:{[^{}]*}&#124;.)*?})

Replace:
```

```
Find:

try\s*?{(.*?)}\s*?catch\s*?\((.*?)\)\s*?{(.*?)}

Replace: $1
```

```
Find:

(class \w*?\s*?{)(.*?String ID;\n*?.*?String fPath;)

Replace: $1
```

```
Find:

(\/\/)(.+?)(?=[\n\r]&#124;\*\))

Replace:
```

```
Find:

/\*.*?\\*/

Replace:
```

3. Save the file after the changes
4. Open the MEC Map Documentation tool and provide the following information
	
	- Select the java file
	- Select the folder where the documentation needs to be saved
	- Enter the Documentation Title
	- Enter the MEC Map version
	- Specify the Author of the Documentation
	- Select the folder where the documentation resources are saved

5. Click the **Generate Documentation** button and wait for the process to finish



## Contact

Get in touch with [Doppio Group](https://doppiogroup.com) or [Ajay Yadukrishnan](mailto:ajayyadukrishnan@gmail.com) to learn more.


## Credits

This project is made possible by the projects listed in this document.

### Contributors

- [Ajay Yadukrishnan](https://github.com/ajayyadukrishnan)

### Libraries

- [tkinter](https://github.com/python/cpython/tree/main/Lib/tkinter)
- [wkhtmltopdf](https://github.com/wkhtmltopdf/wkhtmltopdf)
- [pdfkit](https://github.com/JazzCore/python-pdfkit)
- [PIL](https://github.com/python-pillow/Pillow)
- [pyinstaller](https://github.com/pyinstaller/pyinstaller)


