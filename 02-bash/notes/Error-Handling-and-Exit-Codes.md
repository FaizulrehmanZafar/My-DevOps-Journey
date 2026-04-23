Introduction to Error Handling -
-	Its important as its about foreeing things that could go wrong and able to make appropriate changes before it escalates
-	#!/bin/bash
-	num1=10
-	num2=0
-	result=$((num1 / num2))
-	echo “The result is: $result”
-	./script.sh
-	(Outcome of running the script crashes it as you cant mathematically divide 10 by 0)
-	To Error handle:
-	#!/bin/bash
-	num1=10
-	num2=0
-	if [ $num2 -eq 0 ]; then
-	   echo “Error: Division by zero is not allowed”
-	   exit 1
-	fi
-	result=$((num1 / num2))
-	echo “The result is: $result”
-	./script.sh
-	Error: Division by zero is not allowed (Outcome of running the script)

If statements Recap  –
-	Example of seeing if a file exists in a directory:
-	#!/bin/bash
-	FILE=”/nonexistent”
-	if [[ -f “$FILE” ]]; then
-	    echo “File exists”
-	else
-	    echo “File does not exist”
-	fi
-	./script.sh
-	File does not exist (outcome of running the script)

Exit Codes –

-	Whenever a command or script ends it returns an exit code to the system, it’s a numerical value that represents if the script or command completed successfully
-	#!/bin/bash
-	command -v git 2>/dev/null (checks if a command exists and will send any error messages to dev null)
-	if [[ $? -ne 0 ]]; then (this checks the exit code)
-	   echo “Git is not installed. Please install git”
-	   exit 1
-	else
-	    echo “Git is installed”
-	fi
-	./script.sh
-	Git is installed (outcome of running script)

Set -e –

-	Set -e is a shell option. It stops executing as soon as any command returns a non-zero exit code
-	Using Set -e helps to catch errors as soon as they happen.
-	#!/bin/bash
-	set -e
-	echo “Before the script”
-	nonexistentcommand
-	echo “After the script”
-	./script.sh
-	(Outcome of running script is that it displays “Before the script” but stops after that and displays error that the command: nonexistentcommand is not found)

Set -u –

-	The set -u option forced the script to stop if it encounters an unintitialized variable
-	Also helps to prevent scenarios where missing data could lead to incorrect results or unexpected behaviour
-	#!/bin/bash
-	set -u
-	echo “The value of variable X is: $X” 
-	./script.sh
-	(The outcome of running the script is that it stopped executing and displayed the error about the variable X not being defined)


Set -x –

-	This option prints each command that will be executed to the terminal before it is actually executed
-	Helps the flow of your script and helps to troubleshoot it
-	#!/bin/bash
-	set -x
-	echo “This is a test”
-	X=10
-	echo “The value of X is:10”
-	./script.sh
-	(Outcome of running the script - lists all commands in order)

Set -eux –

-	This will stop the script on an error because of the ‘e’ option, will stop it on a uninitialized variable because of the ‘u’ option and will print each command before execution because of the ‘x’ option
-	#!/bin/bash
-	set -eux
-	echo “This is a test”
-	echo “The value of X is: $X”
-	nonexistentcommand
-	./script.sh
-	(Displays the first command but then stops executing the script and displays error for the second echo as because X is not defined. If X was defined it will then stop at the ‘nonexistentecommand’ command as it’s not a valid command)

More Set Commands –

-	‘Set -o nounset’ also helps to catch uninitialized variables
-	‘Set -o errexit’ this also stops non existing commands
-	‘Set -o pipefail’ this causes a pipeline to return the exit status of the last command in the pipeline that exited with a non-zero status
<img width="936" height="1290" alt="image" src="https://github.com/user-attachments/assets/703030c4-6598-4732-9777-0ab5d7271ec3" />
