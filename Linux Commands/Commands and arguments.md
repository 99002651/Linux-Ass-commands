Practise5: commands and arguments

1. How many arguments are in this line (not counting the command itself).
   touch '/etc/cron/cron.allow' 'file 42.txt' "file 33.txt"
A. 3 arguments.

2. Is tac a shell builtin command ?
A.  type tac -> tac is not a builtin command.

3. Is there an existing alias for rm ?
A. alias rm -> no existing alias.

4. What is -i option of rm. Create and remove a file to test the -i option.
A. man rm
   touch testfile
   rm -i testfile
   
5. Execute: alias rm='rm -i' . Test your alias with a test file. Does this work as expected ?
A. touch testfile
    rm testfile
     
6. List all current aliases.
A. alias

7a. Create an alias called 'city' that echoes your hometown.
A.  alias city="cityname"

7b. Use your alias to test that it works.
A. city

8. Execute set -x to display shell expansion for every command.
A. set -x

9. Test the functionality of set -x by executing your city and rm aliases.
A. set -x
   city
10. Execute set +x to stop displaying shell expansion.
A.  set +x
11. Remove your city alias.
A.  unalias city.

12. What is the location of the cat and the passwd commands ?
A.  which cat -> /usr/bin/cat
    which passwd -> /usr/bin/passwd

13. Explain the difference between the following commands:
    echo
    /bin/echo
A.  echo -> The echo command will interperted by the shell as the builtin echo command.
    /bin/echo -> This command will make the shell execute the echo binary located in the /bin.
    
14. Explain the difference between the following commands:
    echo Hello
    echo -n Hello
A.  The -n option of the echo command will prevent echo from echoing a trailing newline.
    echo Hello will echo six characters in total, echo -n hello only echoes five characters.
    
15. Display A B C with two spaces between B and C.
A.  echo "A B  C"

16. Display (do not use spaces) exactly the following output:
    4+4		=8
    10+14 	=24
A.  echo -e "4+4\t\t=8"
    echo -e "10+14\t=24"
    
17. Use echo to display the following exactly :??\\
    Find two solutions with single quotes, two with double quotes and one without quotes.
A.  echo '??\\' -> ??\\
    echo  ??\\\\ -> ??\\
    echo "??\\\\" -> ??\\    
    
18. Use one echo command to display three words on three lines.
A.  echo -e "one\ntwo\nthree\n"



