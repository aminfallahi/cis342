File management
---

- touch, mv, rm
- chmod: permission bits
- ln: symbolic/hard link

Shell programming
---

- Basics: #! , if , variables , let
	- demo: `#!/bin/bash echo 'hello world';`
			`#!/bin/bash a=1; b=2; a=$a+$b; echo $a;`
			`#!/bin/bash a=2; b=2; let a=$a+$b; echo $a;`
			`if [ $a -gt $b ]; then echo 'a is greater than b'; fi`
	- exercise:
		1. write a script to initialize variable a and b and then swap the values of them
		2. write a script to initialize a and b with some constant value. Then creates a file with the name of the value of the greater variable. For example if a equals 3 and b equals 4, it should create a file named 4.
		3. write a script to initialize three variable a and b and c and then print the sum of them.
- Passing arguments
	- demo: `#!/bin/bash echo $1; echo $2; echo $#;`
	- exercise:
		1. write a bash script to get 3 integers from user and prints the sum of them.
		2. what happens if we do not pass the 3 required integers when executing the bash script we implemented in exercise 1?
		3. write a bash script to gets two file names and swaps the filenames. For example if we input file1 which contains "Alice" and file2 which conains "Bob", after the execution, file1 should contain "Bob" and file2 should contain "Alice".
- Exit values: 
    - demo: `echo alice; echo $?`; rm filenamedttt; echo $?`
    - exercise: 
        1. `touch file111; rm file111; echo $?` what is the output? 
        2. what do you need to do to make `echo $?` print out 1
        3. 
    - homework:
        1. `mkdir fff; echo $?; mkdir fff; echo $?;` why is output different?
        2. can exit code have any other value that 0 and 1? write a program to gets 3 integers and prints the sum of them. If the number of arguments provided are not valid (<>3) the program should exit with code 2.
        3. we want to use the rm command but we don't want to get errors. Write a script to get a file name as a parameter and removes it. If the file does not exist, it should not give an error.
- Commenting

Redirection/Piping
---

- < |
	- demo: `echo 'hello Alice' > somefile`
			`ls -l > somefile`
			`echo 'hello Alice' >> somefile`
			`echo 'somefile' | rm`
	- exercise:
		1. rea
	- homework:
		1. read the man page for 'head' and 'tail' commands. write a bash script to get name of a file and writes the 3 first and 3 last lines of the file to another file named 'output'.
		2. read the man page for 'wc' command. write a bash script to get name of a file and removes it if it contains less that 3 words.
		3. using 'ls' and 'wc' commands, write a single command to print out the number of files in the current directory.
			

Grep & Find
---


Process Management
---

- ps
- top
- Background processes
