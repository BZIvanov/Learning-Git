# Commands

Work in a bash terminal, because the normal one doesn't support all commands like _cat_ for example.

- **pwd** - (print working directory) - will display the currently open directory
- **mkdir folder-name** - will create a new folder in the current directory
- **cd folder-name** - (change directory) will open the specified folder in the current directory
- **ls** - will list the content of the current directory (folders, files etc...). For Windows you should use **dir** (or you can use Windows Power Shell, which supports more commands than the cmd terminal)
- **ls -al** - will list all files include .something files
- **cd ..** - will move one folder back
- **cd ../../** - will move two folders back and so one if we want to go back even more
- **clear** - will clear the text on the console
- **cat ~/myfile.txt** - it allows us to expect the content of a file without opening it. The second parameter is the path to the file.
- **rm -rf folder-name** - will remove the specified folder and all of it's content
- **touch index.js** - will create js file
- **rm index.js** - will remove the specified file
- **> some-file-name.txt** - this command will delete the content of a file. For example navigate to the file's directory and run the command and all text will be deleted and your file will be empty
- **grep sometext some-filename** - this command will search for the text _sometext_ in a file named _some-filename_
