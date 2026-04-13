While loops ‚Äì

-Allow you to repeatedly execute a code unless a certain conditions remain true, example:
-count=1
-while [  -le5 ]
-do
-echo ‚ÄúCount: Äù
-((count++)) (this adds +1 to each iteration until the count reaches 5)
-Done
-./script.sh
-Count: 1 Count: 2 Count: 3 Count: 4 Count: 5 (outcome of executing the script)

For loops ‚Äì

-Allows you to iterate over a sequence of values and perform repetitive tasks
-It‚Äôs a powerful tool for automating operations and processing data
-Enables you to repeat a block of code for a specified number of iterations, example: 
-for (( i=1; i<=5; i++ )) (This will iterate the number from 1 up until it reaches 5)
-do
-echo ‚ÄúNumber: Äù
-done
-./script.sh
-Number: 1 Number: 2 Number: 3 Number: 4 Number: 5 (outcome of executing script)



Break and continue ‚Äì

-These statements allow additional control in ‚Äòfor‚Äô and ‚Äòwhile‚Äô loops
-Allow you to interrupt or break iterations based on specific conditions
-Break example:
-for ((  i=1; i<=5; i++ ))
-do
-    if [  -eq 3 ]
-    then
-       break
-    fi
-    echo ‚ÄúNumber: Äù
-done
-./script.sh
-Number: 1 Number: 2 (outcome of executing script as the break clause prevents the variable ‚Äòi‚Äô from reaching to Number: 5)
-Continue example:
-for ((  i=1; i<=5; i++ ))
-do
-    if [  -eq 3 ]
-    then
-       continue
-    fi
-    echo ‚ÄúNumber: Äù
-done
-./script.sh
-Number: 1 Number: 2 Number: 4 Number: 5 (outcome of executing script as it skips past Number: 3 and continues up to iteration 5)

