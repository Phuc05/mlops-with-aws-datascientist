### Directory operation
```bash
pwd -> current directory
mkdir <directory_name> -> create a directory
ls -> list all items in current folder
ll = ls -l -> with 
cd <child_directory> -> go to the child directory of current directory
cd .. -> go back to parent directory of current directory
cd = cd ~ -> go to /home/User directory
rm -r <directory> -> remove the directory
```
### Copy/Rename/Move operation
```bash
cp A.txt B.txt  -- makes a copy of A.txt names it to B.txt in current directory
cp /home/A.txt /tmp/A.txt -- make a copy of A.txt to /tmp 
cp -r testdir/ newdir/ -- makes a copy of testdir & names it to newdir in current dirctory 
cp -r /home/testdir /tmp/testdir -- makes a copy of testdir to /tmp
cp -p /home/testdir /tmp/non-existed-dir/testdir -- make a copy of test dir and create any folder that not existed yet

mv A.txt new.txt --- renames A.txt to new.txt in current path
mv A.txt /tmp --- moves to A.txt to /tmp
mv testdir newdir -- renames testdir to newdir in current path 
mv newdir /tmp --- moves newdir to /tmp path
```

### File operation
```bash
touch test.txt -> create an empty file
ls -l -> list all contents in current directory
ls -l <directory> -> list all contents in the directory
echo "print hello" -> print out the text in terminal
echo "print hello" > file -> the text to the file (create the file if not existed yet)
echo "print hello" >> file (append new content, not overwrite)
cat file -> write the content of file on terminal and exits page by page
more file -> write the content of file on terminal page by page
less file -> open the file on terminal and can be read line by line
vi file -> visual editor
This opens the file in read only mode
				To edit the file, press 'i' on keyboard for INSERT mode & then you can write anything
				once the text is entered, press 'ESC' on keyboard to return back on readonly mode
				press ':wq' on keyboard -- to save & come out of the file
				press ':q' on keyboard -- to come out of the file without saving
				press ':wq!' on keyboard -- to save forcefully & come out of the file
				press ':q!' on keyboard -- to come out of the file forcefully without saving	
rm -m file -> remove the file
```

### File/directory permission
```bash
Observe the output of ls:
drwxr-xr-x  2 admin  staff   64 Feb 20 19:13 dev
drwxr-xr-x  4 admin  staff  128 Feb 20 19:38 test
-rw-r--r--  1 admin  staff  207 Feb 20 19:19 test.txt
drwxrwxr-x or -rw-rw-r--   --> Read/Write/Execute Permission for a file or a directory in linux
(1st value)admin - owner of the file/directory
(2nd value)staff - group who owns file/directory 
how to update the owner & group for a file/dir 

chown ( change owner ) is the command to update the owners of dir/file 
note: note that you need to have previliges to update the permissions for a file/directory
	
Syntax: chown owner:group filename/dirname
chown murthy:development filename/dirname --> updates the owner & group of the file/directory to murthy & development
```
how to update the read,write & execute permissions for a file/dir
```bash
	How to decode the Read/Write/Execute Permission terminology: 
	-/d    ---> denotes if it is a file or directory ( - means file / d means directory ) 
	rwx    ---> means read,write & execute permissions for super user ( root )
	rw-    ---> means read,write permissions for the owner of the file ( ex: manifoldailearning as above )  
	r--    ---> means read only permissions for others ( whoever login to the machine ) 


	r  -- Permission to read the file.
	w  -- Permission to write (or delete) the file.
	x  -- Permission to execute the file, or, in the case of a directory, search it.

	chmod ( change mode ) is the command to update the read/write/execute permissions for a file/directory
	r = 4, w = 2, x = 1
	
	- | rwx  | rwx  | rwx
	- | 421  | 421  | 421
	
	to update the permissions we can sum 421 
	if super user needs to have read,write & exeute give 7 
	if the owner need to read & write give 6 
	if other need to have only read give 4  
		   

	chmod 777 file/dir -- rwx for root, rwx for owner, rwx for others 
	chmod 764 file/dir -- rwx for root, rw for owner, r for others 
	chmod 755 fire/dir -- rwx for root, rw for owner, rw for others
	chmod 400 firl/dir -- r for root, for owner/other no permissions # common reason u would see while ec2 ssh keys
```
