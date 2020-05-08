# Count files and folders of current directory

_#unix_ _#bash_

Let's assume we have 1 folder in our current directory:

```bash
$ ls -al
total 20 # no idea what this is
drwxrwxr-x  5 user user 4096 Apr 29 20:28 .
drwx------ 18 user user 4096 May  6 13:45 ..
drwxrwxr-x  9 user user 4096 Apr  9 19:13 folder
```

We can simply count the lines of the output:

```bash
$ ls -al | wc -l
4 # subtracting 3 => 1 file/folder
```

## Source

- [Ask Ubuntu: Find number of files in folder and sub folders?](https://askubuntu.com/a/34102/466593)
