

# MEC Map Documentation Guide
Guide to use the MEC Map Documentation tool

<link rel="shortcut icon" type="image/x-icon" href="/mec-map-documentation-guide/doppio-icon.ico">
<a href="https://doppiogroup.com/"><img style="float: right;" src="https://doppiogroup.com/wp-content/uploads/2021/04/doppio_hmpg_animation_FNL2.gif"></a>

## Download

Click [here](https://www.dropbox.com/s/bzwdi2ngxs4ix8e/mec-map-documentation.exe?dl=0) to download the executable file.

## Pre-requisites

- MEC Map Documentation Tool
- Notepad++
- MEC Map Current Source File
- [Resource Files](https://github.com/ajayyadukrishnan/mec-map-documentation-guide/raw/main/resources.zip) folder containing the logo, headers, footers, and the cover page

## Instructions

- Get the current source from the MEC and save it as a ***.java*** file
- Open the ***.java*** file in Notepad++ and run the following  steps to remove unnecessary text. Press **Ctrl + H** to open the Find and Replace window. Select **Regular expression** Radio box, **. matches newline** checkbox and also the **Wrap around** checkbox.

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

(class \w*?\s*?{)(.*?String ID;\n*?.*?String fPath;)

Replace: $1
```

```
Find:

void\s*?run\(\)\s*?{\s*?try\s*?{(.*?)}\s*?catch\s*?\((Throwable\s*?t)\)\s*?{(.*?)}\s*?}

Replace: void run\(\){$1}
```

```
Find:

boolean\s*?run\(\)\s*?{\s*?try\s*?{(.*?)}\s*?catch\s*?\((Throwable\s*?t)\)\s*?{(.*?)}

Replace: void run\(\){$1
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


