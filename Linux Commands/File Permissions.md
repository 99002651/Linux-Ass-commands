Practice: standard file permissions
1. As normal user, create a directory ~/permissions. Create a file owned by yourself in there.
A. cd ~/permission;touch ~/permission/file.txt

2. Copy a file owned by root from /etc/ to your permissions dir, who owns this file now ?
A.  cp /etc/profile ~/permission/

3. As root, create a file in the users ~/permissions directory.
A. touch /home/user/permission/rootfile

4. As normal user, look at who owns this file created by root.
A. ls -l ~/permission/

5. Change the ownership of all files in ~/permissions to yourself.
A. chown user ~/permissions/*
   You cannot become owner of the file that belongs to root.
   
6. Make sure you have all rights to these files, and others can only read.
A. chmod 644 -> to change the mode on files
   chmod 755 -> to change the mode on directories
   
7. With chmod, is 770 the same as rwxrwx--- ?
A. chmod 770 -> read,write,executable

8. With chmod, is 664 the same as r-xr-xr-- ?
A. chmod 664 -> -rw-rw-r--

9. With chmod, is 400 the same as r-------- ?
A. chmod 400 -> -r--------

10. With chmod, is 734 the same as rwxr-xr-- ?
A.  chmod 734 -> -rwx-wxr--

11a. Display the umask in octal and in symbolic form.
A.   umask ; umask -S
     0002
     u=rwx,g=rwx,o=rx

11b. Set the umask to 077, but use the symbolic format to set it. Verify that this works.
12. Create a file as root, give only read to others. Can a normal user read this file ? Test writing to this file with nano.
13a. Create a file as normal user, give only read to others. Can another normal user read this file ? Test writing to this file with vi.
13b. Can root read this file ? Can root write to this file with vi ?
14. Create a directory that belongs to a group, where every member of that group can read and write to files, and create files. Make sure that people can only delete their own files.
