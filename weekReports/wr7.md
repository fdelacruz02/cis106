---
Name: Francisco De La Cruz
Semester: Fall 23
Course: CIS 106 Linux Fundamentals
---

# Week Report 7

## cat
* This command is used to display the contents of a file
* cat/option/file
  * `cat file.txt`
    * displays the content of file.txt
  * `cat -n file.txt`
    * displays the content of file.txt with lines numbered

## tac
* This command is used to display the contents of a file in reverse order
* tac/option/file
  * `tac file.txt`
    * display the content of file.txt from end to beginning
  * `tac -b file.txt`
    * displays the content of file.txt with separator before instead of after

## head
* this command is also used the contents of a file. This one by default list the first 10 lines of a file
* head/option/file
  * `head file.txt`
    * displays the first 10 lines of file.txt
  * `head -n17 file.txt`
    * displays the first 17 lines of file.txt


## tail
* this command is also used to display the contents of a file. This one by default list the last 10 lines of a file
* tail/option/file
  * `tail file.txt`
    * displays the last 10 lines of file.txt
  * `tail -n25 file.txt`
    * displays the last 25 lines of file.txt

## cut
* this command is used to pull text from files or outputs
* cut/option/file
  * `-cut -d: -f1,6 /etc/passwd`
    * removes the second to fifth field from the etc/passwd file using the : as the delimiter instead of tab
  * `cut -b 2 file.txt`
    * prints out the first two bytes of each line in file.txt

## paste
* this command is used to concatenate the content of join
* paste/option/files
  * `paste file1.txt file2.txt`
    * joins the content of file1 and file2
  * `paste -d "+" file1.txt file2.txt`
    * joins the content of file1 and file2 with + as the delimiter between the join

## sort
* this command is used to sort assets
* sort/option/file
  * `sort file.txt`
    * sorts the contents of file.txt in alphabetical order
  * `sort file.txt -o sorted_file.txt`
    * `sorts the contents of file.txt and outputs the results to a new file called sorted_file.txt`

## wc
* this command is used to list the number of lines, word, and bytes in a file
* wc/option/file
  * `wc -c file.txt`
    * lists home many bytes are in file.txt
  * `wc -l file.txt`
    * list how many lines are in file.txt

## tr
* this command replaces the contents of a file and displays it but does not save it
* tr/option/file
  * `cat file.txt | tr 'a-z 'A-Z'`
    * replaces the lowercase characters in file.txt to uppercase
  * `cat file.txt | tr [:upper:] [:lower:]`
    * does the same as the previous example but using character classes

## diff
* this command shows you the difference between two files line by line
* diff/option/files
  * `diff -y file1.txt file2.txt`
    * displays the difference between file1 and file2 side by side
  * `diff -q file1.txt file2.txt`
    * displays the difference beween file1 and file2 only when the files are not identical

## grep
* this command is used to search for a word in a file and shows you every instance that that word appears
* grep/option/files
  * `cat /etc/passwd | grep bash`
    * this displays every instance of bash in the etc passwd file
  * `cat file.txt | grep -i this`
    * this displays every instance of the word this in file.txt

## awk
* this is a language that is used to filter and manipulate output
* awk/option/files
  * `whereis bash | awk '{print$2}'`
    * this redirects the output of the location of bash and prints the second field
  * `awk '{print}' file.txt`
    * this prints the contents of file.txt
  * `awk 'NR>1 && NR < 4' file.txt`
    * this prints the lines 2 and 3 from file.txt
  * `awk 'NR>1' file.txt1`
    * this prints all lines except the first of file.txt
  * awk 'NF' file.txt
    * this command removes some of the whitespace from file.txt

## sed
* this a command that allows you to manipulate text
* sed/option/file
  * `echo "hello, world" | sed 's/hello/goodbye/'`
    * prints out goodbye, world
  * `echo "life is good" | sed 's/good/bad/'`
    * prints out life is bad
  * sed 's/first/last/g' file.txt
    * replaces every instance of first with last in file.txt
  * `sed -n '1,4p' file.txt`
    * prints out lines 1 to 4 file.txt
  * `sed -n -e '1,4p' -e '2,3p' file.txt`
    * prints out lines 1,4,2, and 3 from file.txt



