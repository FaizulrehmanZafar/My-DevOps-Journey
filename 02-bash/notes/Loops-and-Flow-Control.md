While loops -

-Allow you to repeatedly execute a code unless a certain conditions remain true, example:
#!/bin/bash
-count=1
-while [ $count -le5 ]
-do
-echo "Count: $count"
-((count++)) (this adds +1 to each iteration until the count reaches 5)
-Done
-./script.sh
-Count: 1 Count: 2 Count: 3 Count: 4 Count: 5 (outcome of executing the script)

For loops -

-Allows you to iterate over a sequence of values and perform repetitive tasks
-Itâ€™s a powerful tool for automating operations and processing data
-Enables you to repeat a block of code for a specified number of iterations, example: 
#!/bin/bash
-for (( i=1; i<=5; i++ )) (This will iterate the number from 1 up until it reaches 5)
-do
-echo "Number: $i"
-done
-./script.sh
-Number: 1 Number: 2 Number: 3 Number: 4 Number: 5 (outcome of executing script)



Break and continue -

-These statements allow additional control in â€˜forâ€™ and â€˜whileâ€™ loops
-Allow you to interrupt or break iterations based on specific conditions
-Break example:
#!/bin/bash
-for ((  i=1; i<=5; i++ ))
-do
-    if [ $i -eq 3 ]
-    then
-       break
-    fi
-    echo "Number: $i"
-done
-./script.sh
-Number: 1 Number: 2 (outcome of executing script as the break clause prevents the variable â€˜iâ€™ from reaching to Number: 5)
-Continue example:
-for ((  i=1; i<=5; i++ ))
-do
-    if [ $i -eq 3 ]
-    then
-       continue
-    fi
-    echo "Number: $i"
-done
-./script.sh
-Number: 1 Number: 2 Number: 4 Number: 5 (outcome of executing script as it skips past Number: 3 and continues up to iteration 5)

