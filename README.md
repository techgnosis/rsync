# rsync notes

`rsync -avzh <source> <destination>`  
The source directory itself, including its contents, will be copied into the destination directory

`rsync -avzh <source>/ <destination>`  
If there is a trailing slash after the source directory then only the contents of the source directory will be copied into the destination directory  

Add the `--dry-run` flag to see what will get moved before you commit


The `-a` flag is the same as `-rlptgoD`

`-r` is --recursive

`-l` is `--links` which copies symlinks

`-p` is `--perms` which copies permissions

`-t` is `--times` which copies modification times

`-g` is `--group` which transfers group ownership

`-o` is `--owner` which transfers file ownership

`-D` is `--devices --specials` which transfers device files and special files like sockets

`-v` is `--verbose` which tells you what files are being copied in real time

`-z` is `--compress` which compresses files during transfer

`-h` is `--human-readable` which shows bytes in human readable formats

I think the ideal command for backing up files to an external drive is

```
rsync \
--recursive \
--perms \
--times \
--group \
--owner \
--verbose \
--compress \
--human-readable
```

I don't want `--links`, `--devices`, or `--specials`
