Commands:
=========

cd -  change directory
clear - clears the screen
$ - normal user (do not have previleges like root)
pwd - present working directory

sudo su - root access(we will login in the home directory of normal user)
[ ec2-user@<ip> ~ ]$ sudo su
[ root@<ip> /home/ec2-user ]# (# - super user)
[ root@<ip> /home/ec2-user ]# who am i
ec2-user pts/0        2026-03-19 12:57 (124.123.166.186)
[ root@<ip> /home/ec2-user ]# exit
[ ec2-user@<ip> ~ ]$

uname --> print os/kernel info
uname -a --> (single hyphen for character)
uname --all --> (double hyphen for word)

ls - list subdirectories
ls -l - lists in long format
ls -lr - reverse order
ls -lt - latest files on top
ls -ltr - latest files on bottom
cd - goes to home dir from anywhere
cd .. - to come out of current directory
ls -a - shows the hidden files (hidden files start with .)
ls -lart - hidden files and folders

touch devops.txt --> to create a file
mkdir(make directory) devops --> to create a directory(folder)
[ ec2-user@<ip> ~ ]$ cat > devops.txt
linux-practice (write content here)
----press ctrl+d here----
[ ec2-user@<ip> ~ ]$ cat devops.txt (to read the content)
linux-practice
cat >> devops.txt -  to append the text to existing content
> - redirection, usually overrides the content
>> - appends to the previous text

rm devops.txt - to remove a file
rmdir devops - remove the directory

cp(copy) <source> <destination> - copy the file
ex: cp aws.txt devops/
mv aws.txt devops/ -  to move the file
mv aws.txt aws-1.txt - to rename the file
mv aws.txt devops/aws-2.txt - we can move the file as well as rename the file

Downloading files or software:
------------------------------
wget and curl

wget(web get) <url> - to download the software
curl <url> - curl will not download package by default it display content on screen
curl is used to hit api urls
we can do CRUD operations with curl
curl -k <url> > <filename> - to download using curl

grep - command to search inside file
grep <word-to-search> <filename>
grep -n <word-to-search> <filename> - display line numbers
grep -i <word-to-search> <filename> - to deal with case insensitive
grep -c <word-to-search> <filename> - to display no.of occurences
grep -v <word-to-search> <filename> - non-matching

$ - ending character
^ - starting character
history - shows all previously ran commands
ctrl+r - search for word you can see commands used

head <filename> - gives top 10 lines by default
tail <filename> - gives bottom 10 lines by default
head -n 3 <file> - disaply first 3 lines of file
tail -n 3 <file> - display last 3 lines of file
tail -f <file> - follow the log

Piping(|): i/p-----------o/p i/p-------------o/p
ex: cat <file> | grep "word"

cut & awk: 
----------
used for text processing and data extraction in Linux/Unix shells.
ex: 
[ ec2-user@<ip>~ ]$ cat > cut.txt
https://raw.githubusercontent.com/torvalds/linux/master/fs/proc/cmdline

[ ec2-user@<ip> ~ ]$
[ ec2-user@<ip> ~ ]$ cut -d "/" -f1 cut.txt
https:

-d --> delimitter
-f --> fragment
cut -d "/" -f1-5 cut.txt

cat /etc/passwd --> get the list of users
cut -d ":" -f1 /etc/passwd
cut -d ":" -f1,3 /etc/passwd
cut -d ":" -f1-3 /etc/passwd

awk is advanced than cut
syntax : awk -F "/" '{print $NF}'
F - Fragment
N - nth fragment
awk -F ":" '{print $1F}' /etc/passwd
awk -F ":" '{print $1F,$3F}' /etc/passwd

vim editor(visually improved):
----------------------------------
vim is advanced than vi
vim <file_name> - open the file if exists
                  create and open the file if not exists
Modes in vim/vi:
esc mode(press Esc)
insert mode(press i)
command/colon mode(press :)

vim features:
:q! --> to come out of file
:wq! --> save and come out of file
:set nu --> display line numbers
:<line_number> --> to go to specific line number
:/<word> --> to search for word from top to bottom
:?<word> --> to search for word from bottom to top
:<line_number>d --> deletes the particular line
:noh --> no highlight








