---
Name: Francisco
Semester: Fall 23
Course: CIS 106 Linux Fundamentals
---

# Week Report 6

## Wildcards

### *
* The Star wildcard is both extremely useful and dangerous. 
* It has an infinite scope.
* It can be used to do tasks quickly.
  * `ls *.txt`
    * this command lists all the txt files in the present working directory
  * `rm ~/Downloads/Delete/*.png`
    * this command deletes all the png files in the Delete directory
  * `mv *garcia.doc ~/Documents`
    * this moves every file that ends with garcia.doc to the Documents directory

### ?
* The Question mark wildcard has a scope of 1.
  * `ls CIS-???/`
    * this list all the files in the cis106 directory
  * `mv wr?.* ~/cis106/weekreports/`
    * this moves all week report files(excluding images) to the cis106 weekreports directory
  * `rm wr?.??`
    * this deletes all week report markdown files in the cis106 directory

### []
* The Brackets wildcard has a scope of 1 and will match a specified range.
  * `ls ~/cis106/lab[0-9]`
    * lists the contents of all lab folders in the cis 106 repository
  * `ls [[:punct:]]`
    * lists hidden files in the present working directories
  * `mv b[ae]ll.png Pictures`
    * from the home directory moves bell.png and ball.png to the pictures directory

## Practice

### Practice 5
[practice 5](wr6.p1.png)<br>

### Practice 6
[practice 6](wr6.p2.png)<br>

### Practice 7
[practice 7](wr6.p3.png)<br>

## Brace Expansion
* Brace expansion allows you to create, delete, and move files in a simplified manner
  * `mkdir -p ~/Downloads/{directory1,directory2,directory3}/`
    * creates 3 directories in the Downloads directory
  * `mv ~/Downloads/{directory1,directory2,directory3} ~`
    * moves directory 1-3 to the home directory
  * `rmdir {directory1,directory2,directory3}/`
    * deletes directory 1-3





