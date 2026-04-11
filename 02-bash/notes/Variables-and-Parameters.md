Variables –

-Variables are created using ‘=’
-They allow you to store and manipulate data allowing your script to be dynamic and flexible
-To create variables go into your bash script:
#!/bin/bash
-greeting="Hello World!" (creates the variables for greeting)
-count=10 (creates a variable for count)
-fruits=(“apple, banana, oranges”) (this creates a variables for multiple arrays)
-echo $greeting
-echo $count
-echo $fruits
-:wq!
-chmod +x script.sh
-./script.sh
-Hello World! (outcome of running script)
-10 (outcome of running script)
-apple, banana, oranges (outcome of running script)

Parameters – 

-Allows you customise the behaviour of your script and makes it more flexible
-To run a parameter,  you run it within the same line of executing your script, example:
-./script.sh parameter1 parameter 2
-How to create parameters:
#!/bin/bash
-Echo “Parameter 1: $1”
-Echo “Parameter 2: $2”
-./script.sh hello hi
-Parameter 1: hello (outcome of executing script)
-Parameter 2: hi (outcome of executing script)

Arithmetic Expansion –

-You can perform calculations within the arithmetic expression: $(( ))
-This increases flexibility and makes scripts more dynamic
#!/bin/bash
-num1=5
-num2=10
-result=$((num1 + num2))
-echo “The sum of  and  is: $result"
-:wq!
-./script.sh
-The sum of 5 and 10 is: 15 (outcome of executing the script)
#!/bin/bash
-length=5
-width=8
-area=$((length * width))
-perimeter=$((2 * (length + width)))
-echo “Rectangle area: $area"
-echo “Rectangle perimeter: $perimeter"
-:wq!
-./script.sh
-Rectangle area: 40 (outcome of executing the script)
-Rectangle perimeter: 26 (outcome of executing the script)