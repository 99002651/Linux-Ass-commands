Practice : links
1. Create two files named winter.txt and summer.txt, put some text in them.
A. echo winter is cool >winter.txt;echo summer is hot .summer.txt

2. Create a hard link to winter.txt named hlwinter.txt.
A. ln winter.txt hlwinter.txt

3. Display the inode numbers of these three files, does the hard links have the same inode?
A. ls -li winter.txt summer.txt hlwinter.txt

4. Use the find command to list the two hardlinked files
A. find -links -type f
5. Everything about a file is in the inode, except two things : name them!
A. The name of the file is in a directory, and the contents is somewhere on the disk.

6. Create a symbolic link to summer.txt called slsummer.txt.
A. ln -s summer.txt slsummer.txt

7. Find all files with inode number 2. What does this information tell you ?
A. It tells you there is more than one inode table (one for every formatted partition + virtual file systems)


8. Look at the directories /etc/init.d/ /etc/rc2.d/ /etc/rc3.d/ ... do you see the links ?
A.  ls -l /etc/init.d/ -> init.d is the sub-directory of /etc directory in Linux file system. init.d basically contains the bunch of  
    start/stop scripts which are used to control (start,stop,reload,restart) the daemon while the system is running or during boot. If you 
    look at /etc/init.d then you will notice all the scripts for different services of your system. 
    
    ls -l /etc/rc2.d/ -> run control script
    ls -l /etc/rc3.d/

9. Look in /lib with ls -l...
A. ls -l /lib

10. Use find to look in your home directory for regular files that do not(!) have one hard link.
A.  find ~ ! -links 1 -type f
