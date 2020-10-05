practice: Redirection
1. Store error from a command to file.

command-name 2> error.txt
command-name 2> stderr.txt


2. Store output from a command to file.

command-name > o/p.txt
command-name > stdo/p.txt

3. Create a log file and append the errors to that file.

command-name 2>> o/p.txt

4. Feed inline input to a command
(a)					(b)
var=1			----|---	cat <myfirstscript>
echo $var		----|---

5. Feed output of one command as input to another.

 command1 | command2
 
6. Run a command that gives one output and one error.

command >o/p.txt 2>filename.txt

7. Store output to a file and redirect error to display in the above command.

command-name > o/p.txt
command-name 2> command2


