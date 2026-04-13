If Statements –

-Allow you to introduce decision making logic into your scripts based on specific conditions
-If statement starts with an ‘if’ and ends with ‘fi’, example:
-age=25
-if [  -gt 18 ] (-gt means greater than)
-then
-echo “You are an adult”
-fi
-./script.sh
-“You are an adult” (outcome of executing the script)
-Using logical operators to make more complex conditions, example:
-grade=95
-if [  -ge 90 ] && [  -le 100 ] (The double ‘&&’ is a logical operator that represents AND. The ‘-ge’ stands for greater or equal to. The ‘-le’ stands for less than or equal to. Both these conditions have to be met or the echo string will not execute)
-then
-echo “Excellent”
-fi
-./script.sh
-Excellent (outcome of executing script as both conditions are met)

Else and Elif –

-Provides an alternative path in the script
-The ‘else’ clause gives you an alternative if the conditions to ‘if’ are not met
-age=15
-if [  -gt 18 ]
-then
-echo “You are an adult”
-else
-echo “You are not an adult”
-fi
-./script.sh
-You are not an adult (outcome of executing script because the ‘if’ condition was not met so the ‘else’ string is executed instead)
-The ‘elif’ clause is like adding multiple ‘if’ conditions, example:
-score=85
-if [  -ge 90 ]
-then
-echo “Excellent”
-elif [  -ge 80 ]
-then
-echo “Good”
-else
-echo “Better luck next time”
-fi
-./script.sh
-Good (outcome of executing script as the ‘if’ condition failed but the ‘elif’ condition passed and the ‘else’ clause is there as a failsafe if both ‘if’ and ‘elif’ conditions failed)

Nested if Statements –

-Allows you to create more complex structure that allows you to introduce if statements into another if statement, example: 
-age=19
-grade=85
-if [  -gt 18 ]; then
-echo “You are eligible based on age”
-if [  -ge 80 ]; then
-echo “You are eligible based on grade”
-echo “
-else
-echo “Sorry your grade is not eligible”
-fi
-else
-echo “Sorry, you are not eligible for the scholarship”
-fi
-./script.sh
-You are eligible based on age. You are eligible based on grade. Congrats! You are eligible for the scholarship! (outcome of executing the script as all the nested ‘if’ statements passed the conditions)

