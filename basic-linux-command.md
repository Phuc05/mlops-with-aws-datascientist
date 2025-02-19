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

```