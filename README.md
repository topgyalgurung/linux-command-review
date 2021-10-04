# linux-command-review
> in progress

# [Operating Systems and You: Becoming a Power User by Google](https://www.coursera.org/learn/os-power-user)

### Supplement Reading Resources:
- [bash](https://www.gnu.org/software/bash/manual/bash.html)
- [vim](https://vim.sourceforge.io/docs.php)
- [nano](https://www.nano-editor.org/)
- [emacs](https://www.gnu.org/software/emacs/tour/)
- 

## Week 1: 

  #### a. Basic commands 
  ```
      ls / - list root directory folders
      ls -l
      ls -ld 
      etc stores system configuration
      bin - binary files 
      home - personal directory 

      / - root
      pwd
      cd 
      cd ../ 
      ~ home dir
      mkdir
      mkdir my\ file or mkdir 'my file'
      history
      Ctrl -R to search through history 
      clear

      > copy:
      cp source_file target
      cp *.png~/Desktop
      cp -r   # recursive copy

      > remove:
      rm 
      rm -r
      rm -rf
  ```
  
   ### b. File and Text Manipulation:
    ```
      cat - view file
      less
      more
      head
      tail (last 10 lines)

      search through files:
      grep

      echo
      echo woof>> dog.txt
      cat < file.txt
      ls /dir/fake_dir 2>error
      ls -la /etc | grep bluetooth
    ```

## Week 2: 

### a. Users and Groups
``` 
sudo cat /etc/sudoers # beware 
sudo su -     # substitute user, default to root if not specified
exit
cat /etc/group
cat /etc/passwd

linux password:
sudo passwd -e tinzin # expire user password
sudo useradd name
sudo userdel name
```
### b. Permissions:
```
rwx - read write execute
rwxrw-r-- # rwx for root, rw for group specified, r for all other user

modifying permissions:
o-owner, g- group , o - other user
chmod u-x myfile
chmod u-x myfile
chmod ugo+r myfile 

numerical equivalent 'saves time' 
4- read
2-write
1- execute 

chmod 754 mycoolfile # 4+2+1=7 rwx permission for root, 5 for group, 4 for others
sudo chown name my_file # change owner
sudo chgrp best_group my_file # change group owner

# setUID - allow file to be run as owner of file ( s
, setGID - allow to run file as member of file group (s or 2,1) 
 stickybit - allow file to be written to by anyone but only removable by owner or root (t or 1)

sudo chmod u+s my_file
sudo chmod 4755 my_file # in numerical form use 4 for root, 2 for group  2755 or g+s 
sudo chmod 1755 my_folder/  or chmod +t ..
```
