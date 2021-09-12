
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

3. Save the file after the changes
4. Open the MEC Map Documentation tool and provide the following information
	
	- Select the java file
	- Select the folder where the documentation needs to be saved
	- Enter the Documentation Title
	- Enter the MEC Map version
	- Specify the Author of the Documentation
	- Select the folder where the documentation resources are saved

5. Click the **Generate Documentation** button and wait for the process to finish
