# rsync notes

`rsync -avzh <source> <destination>`  
The source directory itself, including its contents, will be copied into the destination directory

`rsync -avzh <source>/ <destination>`  
If there is a trailing slash after the source directory then only the contents of the source directory will be copied into the destination directory  

Add the `--dry-run` flag to see what will get moved before you commit
