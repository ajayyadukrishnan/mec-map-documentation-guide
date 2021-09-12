

# MEC Map Documentation Guide
Guide to use the MEC Map Documentation tool

<link rel="shortcut icon" type="image/x-icon" href="/mec-map-documentation-guide/doppio-icon.ico">
<a href="https://doppiogroup.com/"><img style="float: right;" src="https://doppiogroup.com/wp-content/uploads/2021/04/doppio_hmpg_animation_FNL2.gif"></a>

## Pre-requisites

- MEC Map Documentation Tool
- Notepad++
- MEC Map Current Source File
- Resource Files folder containing the logo, headers, footers, and the cover page. [Download](https://github.com/ajayyadukrishnan/mec-map-documentation/raw/main/resources.zip)

## Instructions

- Get the current source from the MEC and save it as a ***.java*** file
- Open the ***.java*** file in Notepad++ and run the following  steps to remove unnecessary text. Press **Ctrl + H** to open the Find and Replace window. Select **Regular expression** Radio box and **. matches newline** checkbox

```
Find:

((?:(?:public|private|protected|static|final|abstract|synchronized|volatile)\s+)*)\s*(void|String)\s*(clearIn|clearOut|printOutput|printInput|getErrorMsg)\(.*?\)\s*({(?:{[^{}]*}|.)*?})

Replace:
```

```
Find:

((?:(?:public|private|protected|static|final|abstract|synchronized|volatile)\s+)*)\s*(\w+)\s*\(String ID, String fPath\)\s*({(?:{[^{}]*}|.)*?})

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

(\/\/)(.+?)(?=[\n\r]|\*\))

Replace:
```

```
Find:

/\*.*?\\*/

Replace:
```

- Save the file after the changes
- Open the MEC Map Documentation tool and provide the following information
	
	- Java File Path - *Select the java file*
	- Documentation Folder Path - *Select the folder where the documentation needs to be saved*
	- Documentation Title - *Enter the Documentation Title*
	- Map Version - *Enter the MEC Map version*
	- Author - *Specify the Author of the Documentation*
	- Resources Folder Path - *Select the folder where the documentation resources are saved*

- Click the **Generate Documentation** button and wait for the process to finish



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


