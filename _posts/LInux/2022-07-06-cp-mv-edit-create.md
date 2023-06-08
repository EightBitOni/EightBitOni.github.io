---
title: Linux cp, mv, edit, create commands
author: EightBitOni
date: 2022-06-07 00:00:00 -0600 # year, day, month
categories: [Linux,Commands]
tags: [linux,commands] # all lower case
pin: true

---

## Working with files


### copy file/folder  


```shell
cp (filename/folder) (directory)
```

>[!Note]-
>(remember, if the filename/folder name has spaces then you will need to encase the filename with speech marks such as cp "(filename with spaces)" (directory). This applis to other commands such as mv. )  

```shell
cp ssh.conf /home/newfolder 
```
---

### move file/folder  

mv (filename) (directory)  

example
```shell
mv ssh.conf /home/newfolder  
```
---

### move multiple files/folders simultaneously  

mv (file1) (file2) (file3) -t (directory to move to)

example
```shell
mv logs.txt keys.conf script.py -t /home/savedWork
```
---

### Move all files from current directory into another directory  

mv * (directory to move files to)  

example
```shell
mv * /home/scripts  
```
---
### rename files/folder  

mv (current filename) (new filename)  

example
```shell
mv ssh.conf NewSSH.conf  
```
---
### create a file  

touch (filename)  

example
```shell
touch newFile.txt  
```
---
### create a folder  

mkdir (foldername)  

example
```shell
mkdir newFolder
```
---
### open file for editing  

nano (filename)  

example
```shell
nano keys.conf
```
---
### output contents of file  

cat (filename)  

example
```shell
cat keys.conf  
```
---
### upload file to a remote machine  

scp (filename) (username)@(IP of remote machine ):/(directory to upload to)

example
```shell
scp example.txt john@192.168.100.123:/home/john/
```
---
### run an bash script program  

./(name of script)  

example
```shell
./timer  
```
---
### open a file for reading/editing  

nano (filename)  

example
```
nano readME.txt
```
---
### More Notes

files/folders with special characters such as - (dash), if you try to copy or move these files you will encounter errors because Linux interprets the - as a type of argument, therefore you will have to place -- just before the filename. 

example
```shell
cp -- -filename.txt /home/folderExample.
```