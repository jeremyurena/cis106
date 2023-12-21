# Final Assignment

## Question 1

### awk Command
Description:
* awk is a scripting language used for processing and displaying text.
Formula/Syntax:
* `awk + options + {awk command} + file + file to save (optional)`
Examples:
* Example 1: Print the first column of the every line of a file
  * `awk '{print $1}' ~/Document/Csv/cars.csv`
* Example 2: Print first field of /etc/passwd file
  * `awk -F: '{print $1 $NF}' /etc/passwd`
* Example 3: Print first and last field of the /etc/passwd
  * `awk -F: '{print $1," = ",$NF}' /etc/passwd`

### cat Command
Description:
* cat is used for displaying the content of a file.
Formula/Syntax:
* `cat + option + file(s)_to_display`
Examples:
* Example 1: Display the content of a file using absolute path
  * `cat ~/Documents/todo.lst`
* Example 2: Display the content of a file with line numbers excluding empty lines
  * `cat -b ~/Documents/todo.md`
* Example 3: Display the content of a file with a $ at the end of every line
  * `cat -E ~/Documents/todo.md`

### cp Command
Description:
* cp is used for copying files/directories from a source to a destination.
Formula/Syntax:
* `cat + files_to_copy + destination`
Examples:
* Example 1: Copying a file
  * `cp Download/wallpapers.zip Pictures/`
* Example 2: Coping the content of a directory to another directory
  * `cat -b ~/Documents/todo.md`
* Example 3: Display the content of a file with a $ at the end of every line
  * `cat -E ~/Documents/todo.md`

### cut Command
Description:
* cut is used to extract a specific section of each line of a file and display it to the screen.
Formula/Syntax:
* `cut + option + file(s)`
Examples:
* Example 1: Displaying a list of all users in a system.
  * `cut -d ':' -f1 /etc/passwd`
* Example 2: Cutting a file using a delimiter but changing the delimiter in the output.
  * `cut -d ':' -f1,8 --output-delimiter=" => ' /etc/passwd`
* Example 3: Cutting a file excluding a given field.
  * `cut -d ',' --complement -s f3 users.txt`

### grep Command
Description:
* grep is used to search text in a given file.
Formula/Syntax:
* `grep + option + search criteria + file(s)`
Examples:
* Example 1: Search any line that contains the word "dracula" in the given file
  * `grep 'dracula' ~/Documents/dracula.txt`
* Example 2: Search for all the lines that do not contain the word 'war'
  * `grep -v 'war' ~/Documents/Books/war-and-peace.txt`
* Example 3: Search and match only the word
  * `grep -o 'dracula' ~/Documents/Books/dracula.txt`

### head Command
Description:
* head displays the top N number of lines of a given file.
Formula/Syntax:
* `head + option + file(s)`
Examples:
* Example 1: Displaying first 10 lines of a file.
  * `head ~/Documents/Books/dracula.txt`
* Example 2: Displaying first 5 lines of a file.
  * `head -5 ~/Documents/Books/dracula.txt`
* Example 3: Displaying first 2 lines of a file.
  * `head -2 ~/Documents/Books/dracula.txt`

### ls Command
Description:
* ls is used for displaying all the files inside a given directory.
Formula/Syntax:
* `ls + option + directory to list`
Examples:
* Example 1: Long listing all files inside a given directory recursively.
  * `ls -lR ~/Pictures`
* Example 2: List all the files in a given directory sorted by last modified.
  * `ls -t ~/Documents`
* Example 3: List all the files in a given directory sorted by extension.
  * `ls -X ~/Documents`

### man Command
Description:
* man is used for viewing the manual of a command type.
Formula/Syntax:
* `man + command`
Examples:
* Example 1: Executable programs.
  * `man ls`
* Example 2: Games.
  * `man tetravex`
* Example 3: File formats and conventions.
  * `man passwd`

### mkdir Command
Description:
* mkdir is used for creating a single directory or multiple directories. 
Formula/Syntax:
* `mkdir + name of directory`
Examples:
* Example 1: Creating a directory in the present working directory.
  * `mkdir wallpapers`
* Example 2: Creating a directory in a different directory using absolute path.
  * `mkdir ~/wallpapers/forest`
* Example 3: Creating a directory with a space in the name.
  * `mkdir wallpapers/new\ cars`

### mv Command
Description:
* mv moves and renames directories.  
Formula/Syntax:
* `mv + source + destination`
* `mv + file/directory_to_rename + new_name`
Examples:
* Example 1: Moving a file from a directory to another using relative path.
  * `mv Downloads/homework.pdf Documents/`
* Example 2: Moving a directory from one directory to another using absolute path
  * `sudo mv ~/Downloads/theme /usr/share/themes`
* Example 3: Moving and renaming a file in the same command.
  * `mv Downloads/cis106homework.docx Documents/new_cis106homework.docx`

### tac Command
Description:
* tac is used for displaying the content of a file in reverse order  
Formula/Syntax:
* `tac + option + file(s)_to_display`
Examples:
* Example 1: Displaying the content of a file located in the pwd.
  * `tac todo.md`
* Example 2: Displaying the content of a file using absolute path.
  * `tac ~/Documents/todo.md`
* Example 3: Displaying the content of the users in the system.
  * `tac /etc/passwd`

### tail Command
Description:
* tail is used to display the last N number of lines of a given file.  
Formula/Syntax:
* `tail + option + file`
Examples:
* Example 1: Displaying last 10 lines of a file.
  * `tail ~/Documents/Books/dracula.txt`
* Example 2: Displaying last 5 lines of a file.
  * `tail -5 ~/Documents/Books/dracula.txt`
* Example 3: Displaying last 2 lines of a file.
  * `tail -2 ~/Documents/Books/dracula.txt`

### touch Command
Description:
* touch is used for creating files.  
Formula/Syntax:
* `touch + file(s)`
Examples:
* Example 1: Creating a file called list.
  * `touch list`
* Example 2: Creating several files.
  * `touch list_of_cars.txt script.py names.csv`
* Example 3: Creating a file using absolute path.
  * `touch ~/Downloads/games.txt`

### tr Command
Description:
* tr is used for translating or deleting characters from a standard output.  
Formula/Syntax:
* `standard_output | tr + option + set1 + set2`
Examples:
* Example 1: Translating one character to another.
  * `cat file.txt | tr '.' ','`
* Example 2: Translating white space into tabs.
  * `cat program.py | tr "[:space:]' '\t'`
* Example 3: Translating tabs into space.
  * `cat file.py | tr -s "[:space:]" ' '`

### tree Command
Description:
* tree is used to list the files in a current working directory.  
Formula/Syntax:
* `tree + option`
Examples:
* Example 1: Displaying directory structure of current working directory.
  * `tree`
* Example 2: Listing files with entered pattern.
  * `tree -P sample* .`
* Example 3: Listing the output by last modification.
  * `tree -t`

## Question 2

### How to work with multiple terminals open?
* Use the "add terminals" buttons on the top left of Tilix

### How to work with manual pages?
* Use the arrow keys or the man-command internal shortcuts.

### How to parse (search) for specific words in the manual page?
* Use the grep command

### How to redirect output `(> and |)`
* Ex: `echo "hello world!" > text.txt`

### How to append the output of a command to a file?
* Ex: `echo "hello world!" >> text.txt`

### Using wildcards (copying and moving multiple files at the same time)
* Ex for copying: `cp Download/*.zip Pictures/`
* Ex for moving: `mv Downloads/*.??? Documents/`

### Using brace expansion (for creating entire directory structures in a single command)
* `mkdir -p music/{jazz,rock}/{mp3files,videos,oggfiles}/new{1..3}`