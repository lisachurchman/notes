# Notes

### Entry Template


__command__ - _Description_

__Examples:__

```
bash code in here
```
---

## File Management

__mv__ - _Move file or Rename file_

__Examples:__

```
mv sourceFile destinationFile
mv sourceFile destinationLocation
mv myFile.txt myFolder/
```
---

__cp__ - _Copy file or folder_

__Examples:__

```
cp filename.cpp myCopy.cpp
cp -r myFolder/ myNewFolder

options:
  -p: copy permissions
  -a: copy directory heirarchy recursively, preserving
      all file attributes and links
  -r: copy directory hierarchy; does NOT do a
  -i: interactive mode
  -f: force the copy
```
---

__rm__ - _Remove File_

```
rm (options) files
rm file1 file2
rm -r file1
Note: DO NOT USE rm -r -f File (deletes all files)

options:
  -r:recursively remove directory and contents
```
---

__rkdir__ - _Make a directory_

__Examples:__

```
mkdir (options) directories
mkdir directory1 directory2 directory3
```
---

__rmdir__ - _Remove an empty directory_

__Examples:__

```
rmdir (options) directories
rmdir EmptyDirectory
rmdir -r NonEmptyDirectory
```
---

__ln -s__ - _Symbolic Link or Soft Link; Refers to Another File by its Path_
            _Can point to files on other disk partitions_
            _in general: ln regerence to another file_

__Examples:__

```
ln (options) source target
ln -s myfile mysoftlink
ln -s afile shortcut
ln -s name_A name_B

options:
  -s: symbolic link (soft)
  -d: create hard link to a directory
```
---

__pwd__ - _Prints Absolute Path of Current Directory_

__Examples:__

```
$ pwd
/users/name/directory1
```
---

__ls__ - _Lists Files and Directories in Current Directory_

__Examples:__

```
ls (options)
ls LabFoler
ls -a (Displays Hidden Files)
ls *.txt

options:
  -a: lists all files, dot files (hidden)
  -l: long lasting (file attributes)
  -d: if listing directory, don't list contents, just dir itself
```
---

__tar__ - _Backing Up Files, file-packing_

__Examples:__

```
tar -czvf myarchive.tar.gz mydirectory
tar -xvf myarchive.tar file1 file2

options:
  -c: create and archive
  -r: append files to existing archive
  -u: append changed/new files to existing one
  -x: extract files from archive
  -f file: read archive from file
  -d: diff 
  -z: use gzip compression
  -v: verbose mode: print extra info
```


## File Transfer

__curl__ - _Writes to Standard Output by Default_

__Examples:__

```
curl http://www.yahoo.com/moreinfmation > mypage.html
```
---

__wget__ - _Downloads the Data to a File or Standard Input_

__Examples:__

```
wget url
wget http://www.yahoo.com/informationaboutsomething

options:
  -c: continue mode
```
---

__scp__ - _Secure Copy Copies Files and Directories from One Computer to Another branch_

__Examples:__

```
scp myfile remote.example.com:newfile

recursively copy a directory to a remote machine
$ scp -r mydir remote.example.com:

copy a remote file to your local machine
$ scp remote.example.com:myfile .

recursively copy remote dir to local machine
$ scp -r remote.example.come:mydir .
```
---

__rsync__ - _Copies a Set of Files_

__Examples:__

```
rsync D1 D2
rsync -a D1 D2 (mirroring: copy all attributes of file)
rsync -a -e ssh D1 smith@server.example.com:D2

options:
  -o: copy ownership of files
  -g: copy group ownership of files
  -p: copy permissions
  -t: copy file timestamps
```
---

## Pipe tools

__cat__ - _Show Content of a File_

__Examples:__

```
cat MyFile.txt
cat myprogram.cpp

options:
  -T: print tabs as ^l
  -E: print new lines as $
```
---

__sort__ - _Sort Conents of a File_

__Examples:__
```
sort myfile.txt
sort myfile.txt > sortedfile.txt
sort -n myfile.txt > sorted_by_number.txt

options:
  -f: case-insensitive sorting
  -n: sort numerically
  -u: unique sorting: ignore duplicates
  -c: don't sort just check if input is sorted
      only prints error message
  -b: ignore leading whitespace
  -r: reverse output: greatest to least
```
---

__uniq__ - _Finds Unique Words in a File_

__Examples:__
```
uniq myfile.txt
$ sort myfile | uniq -c
    1 a
    3 b
    1 c
uniq -c myfile.txt (displays the count of of each word)

options:
  -c: count adjacent lines
  -i: case insensitive
  -u: unique lines only
  -d: print dublicates only
```
---

__grep__ - _Search for Text in a File_

__Examples:__
```
grep (text to look for) FileName
grep hello MyFile
grep -i the MyFile (does not consider uppercase)

options:
  -v: print only lines that DO NOT match regular expression
  -l: print only the names of files that containe match NOT LINES THEMSELVES
  -L: print names of files that DO NOT match reg exp
  -c: print count of matching lines
  -n: in front of each line of matching output, print its orig line number
  -i: case insensitive match
  -w: complete words
  -x: complete lines
```
---

## Others gone over for class

__tail__ - _Prints last 10 lines of file_

__Examples:__

```
tail -15 myFile (prints 15 lines not 10)
```
---
__touch__ - _changes timestampts, can create empty files_

__Examples:__

```
touch myfile (set timestamps to rn)
touch -d "November 18 1975" myfile
```
---

__chmod__ - _(Change Mode) protects files and directories from unauthorized users; sets permissions_

__Examples:__

```
to use:
  scope: u for user, g for group, o for users not in group, a for all users
  command: + to add; - to remove, = to set permissions
  permissions: r (read), w (write), x (execute)
```
---
