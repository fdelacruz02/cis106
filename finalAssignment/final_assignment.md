#Final Assignment

## Question 1
Awk 
* description: a language generally used to filter outputs
* awk\option\action\input-file\output-file
  * awk -F: '{print $1, $NF}' /etc/passwd
  * prints the first and last field in the /etc/passwd/ file
  * who | awk -F: '{print $3}'
  * prints the last field out of the who command output
  * date | awk '{print $2,$3,$NF}'
  * prints the second, third and last field of date command output

Cat 
* description: a command to display the contents of a file
* cat\option\filename
  * cat file.txt
  * prints the content of file.txt to the terminal
  * cat -n file.txt
  * prints the contents of file.txt with line numbers
  * cat -E file.exe
  * prints the content of file.txt with $ at the end of each line


Cp
* description: a command to copy files and directories
* cp\option\file\destination
  * cp -r some_directory/
  * copies a directory recursively
  * cp file.txt ~/Documents/
  * copies file.txt to the Documents directory
  * cp file.txt ./
  * copies file.txt to the current directory

Cut
* description: a command to remove a part of a file
* cut\option\file
  * cut -d ' ' file.txt
  * removes every space in file.txt
  * cut -f 2 file.txt
  * removes the second field from file.txt
  * cut -f1,6 /etc/passwd/

Grep
* description: a command to find a specific word in a file
* grep\option\patterns\file
  * grep bash /etc/passwd
  * prints bash from every line int the etc passwd file
  * grep -n bash /etc/passwd
  * prints bash from every line in the etc passwd file with line numbers
  * grep -v bash /etc/passwd
  * prints out all the lines that do not match the term

Head
* description: a command to print out  the beginning of a file
* heads\option\file
  * head file.txt
  * prints the first 10 lines of file.txt 
  * head -n5 file.txt
  * prints the first 5 lines of file.txt
  * head -c4 prints the first 4 bytes of file.txt

Ls
* description: a command list files, directories
* ls\option\path
  * ls
  * list all files and directories in pwd
  * ls -1
  * long list
  * ls -d */
  * list all directories in current directory

Man
* description: a command to read a manual page for a command
* man\option\section\page
  * man ls
  * shows you the manual page for ls command
  * man head
  * shows you the manual page for head command
  * man awk
  * shows you the manual page for the awk command

Mkdir
* description: a command to make directories
* mkdir\option\directory\
  * mkdir place
  * creates a subdirectory called place in your pwd
  * mkdir -p somewhere/over/the/rainbow
  * creates a directory called rainbow and all its parent directories
  * mkdir ~/Documents/deals

Mv
* description: a command to move files, directories, rename file
* mv\option\source\destination
  * mv lost.txt ./found.txt
  * renames the lost.txt file found.txt
  * mv lost.txt ~/Documents/
  * moves the lost.txt to the documents directory
  * mv place/ ~
  * moves the place directory to the Home directory

Tac 
* description: a command to display in reverse order the contents of a file
* tac\option\filename
  * Tac file.txt
  * prints the content of file.txt to the terminal starting with the end of the file
  * Tac -b file.txt
  * prints the contents of file.txt from end to beginning with the separator before the end of the file
  * Tac file.md
  * prints the content of file.txt end to beginning

Tail
* description: a command to print out the end of a file
* tails\option\file
  * tail file.txt
  * prints the last 10 lines of file.txt 
  * tail -n5 file.txt
  * prints the last 5 lines of file.txt
  * head -c4 prints the last 4 bytes of file.txt

Touch
* description: a command that is usually used to create files, can also change access and modification times
* touch\option\file
  * touch file.txt
  * creates file.txt in pwd
  * touch -c file.txt
  * does not create any files
  * touch -t 11110545 file.txt
  * creates a file named file.txt with the creation date as Nov 11th, 2023 at 5:45 am

Tr
* description: a command that is usually used to replace the content of a file
* tr\option\set1\set2
  * cat /etc/passwd | tr ":" " "
  * removes every : from the etc/passwd file
  * echo 'Under Pressure we're Breaking' | tr ' ' '\n'
  * prints Under Pressure we're Breaking with each word on a new line
  * echo "lowercase" | tr '[:upper:]'
  * translates lowercase to LOWERCASE
  * echo "A   B    C    D" | tr -s '[:blank:]'
  * removes some of the space between A B C and D

Tree
* description: a command that displays the file system as a tree
* tree\option\path
  * tree
  * displays the a tree of the pwd
  * tree -a
  * displays a tree of the pwd with all files listed
  * tree -aQ ~/Downloads
  * displays a tree of the Downloads folder, list all files with double quotes around file names

## Question 2

How to work with multiple terminals open?
  * Split the current terminal or you can install a terminal emulator like Terminator, Tilix, or Quake and open another terminal simultaneously.
    * With terminator ctrl+shift+O  and ctrl+shift+E split terminals horizontally(the former) and vertically(the latter)
How to work with man pages?
  * You type man before something you want to know about about and add a number to go to a specific category.
    * 1 is for General commands
    * 2 is for System calls
    * 3 is for Library functions
    * 4 is for Special files
    * 5 is for file formats and conventions
    * 6 is for games
    * 7 is for miscellaneous
    * 8 is for system administration
    * 9 is for kernel routines
How to to parse for specific words in a man page?
  * You should redirect the output to a grep command with the word you are looking for
    * Ex. man ls | grep all
How to redirect output?
  * ">" is used to write the output to a file
    * echo "Hello, World" > file.txt
      * this writes Hello, World to file.txt
  * | is used to redirect the output of a command to another command
    * man tree | grep directory
      * this lists all instances of directory found in the tree man page
How to append to a file?
  * ">>" is used to append the output to a file
    * echo "Hello, World" >> file.txt
      * this adds Hello, World to the end of file.txt
How to use wildcards?
  * to move every .docx file to a folder called reports in the Documents directory
    * mv *.docx ~/Documents/reports/ 
  * To copy every .py that starts with program, ends with py, has a space for the program number
  * Will copy to a folder called cis101 in the Downloads directory
    * cp program?.py ~/Downloads/cis101/
How to use brace expansion?
  * you will use mkdir -p
    * to create a directory musica with two subdirectories called viejo, nuevo who have subdirectories urbana, classicos, especial
      * mkdir -p musica/{viejo,nuevo}/{urbana,classicos,especial}/






