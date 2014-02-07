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
```
---

__rm__ - _Remove File_

```
rm (options) files
rm file1 file2
rm -r file1
Note: DO NOT USE rm -r -f File (deletes all files)
```
---

__rmdir__ - _Make a directory_

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

__Examples:__

```
ln (options) source target
ln -s myfile mysoftlink
ln -s afile shortcut
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
```
---

__tar__ - _Backing Up Files_

__Examples:__

```
tar -czvf myarchive.tar.gz mydirectory
tar -xvf myarchive.tar file1 file2
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
```
---

__scp__ - _Secure Copy Copies Files and Directories from One Computer to Another_

__Examples:__

```
scp myfile remote.example.com:newfile
```
---

__rsync__ - _Copies a Set of Files_

__Examples:__

```
rsync D1 D2
rsync -a D1 D2 (mirroring: copy all attributes of file)
```
---

## Pipe tools

__cat__ - _Show Content of a File_

__Examples:__

```
cat MyFile.txt
cat myprogram.cpp
```
---

__sort__ - _Sort Conents of a File_

__Examples:__
```
sort myfile.txt
sort myfile.txt > sortedfile.txt
sort -n myfile.txt > sorted_by_number.txt
```
---

__uniq__ - _Finds Unique Words in a File_

__Examples:__
```
uniq myfile.txt
uniq -c myfile.txt (displays the count of of each word)
```
---

__grep__ - _Search for Text in a File_

__Examples:__
```
grep (text to look for) FileName
grep hello MyFile
grep -i the MyFile (does not consider uppercase)
```
