## UID: 905797640

# Hey! I'm Filing Here

Implementation of an ext2 filesystem that outputs a mountable image.

## Building

```shell
make # compile the executable
./ext2-create # run the executable to create cs111-base.img
```

## Running

```shell
mkdir mnt # create a directory to mnt the cs111 filesystem to
sudo mount -o loop cs111-base.img mnt # mount the filesystem, loop lets you use a file
```
### Example
```shell
ls -ain
# total 7
#     2 drwxr-xr-x 3    0    0 1024 Jun  1 13:19 .
# 641674 drwxr-xr-x 4 1000 1000 4096 Jun  1 13:19 ..
#     13 lrw-r--r-- 1 1000 1000   11 Jun  1 13:19 hello -> hello-world
#     12 -rw-r--r-- 1 1000 1000   12 Jun  1 13:19 hello-world
#     11 drwxr-xr-x 2    0    0 1024 Jun  1 13:19 lost+found
```

## Cleaning up

```shell
sudo umount mnt # unmount the filesystem when you're done
rmdir mnt # delete the directory used for mounting when you're done
make clean # remove all binary files
```
