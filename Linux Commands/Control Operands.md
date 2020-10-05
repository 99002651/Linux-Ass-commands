Practice6: control operators( ;, &, $?, &&, ||, #, \ )


0. Each question can be answered by one command line!
1. When you type passwd, which file is executed ?
A. which passwd

2. What kind of file is that ?
A. passwd is /usr/bin/passwd

3. Execute the pwd command twice. (remember 0.)
A. pwd;pwd

4. Execute ls after cd /etc, but only if cd /etc did not error.
A. cd /etc && ls

5. Execute cd /etc after cd etc, but only if cd etc fails.
A. cd etc || cd /etc

6. Echo it worked when 'touch test42' works, and echo it failed when the touch failed. 
   All on one command line as a normal user (not root).
   Test this line in your home directory and in /bin/ .
A. user@user-OptiPlex-7040:/bin$ cd ;touch test34 && echo it worked || echo it failed
   it worked
   user@user-OptiPlex-7040:~$ cd /bin;touch test34 && echo it worked || echo it failed
   touch: cannot touch 'test34': Permission denied
   it failed

7. Execute sleep 6, what is this command doing ?
A. Pausing for 6 seconds.

8. Execute sleep 200 in background (do not wait for it to finish).
A. sleep 200 &

9. Write a command line that executes rm file55. Your command line should print 'success'
   if file55 is removed, and print 'failed' if there was a problem.
A. rm file55 && echo success || echo failed

10. Use echo to display "Hello World with strange' characters \ * [ } ~ \\ .(including all quotes)passwd is /usr/bin/passwd
A.  echo "Hello World with strange' characters \ * [ } ~ \\\\ ."



