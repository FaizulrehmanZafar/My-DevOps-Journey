Basics of function –

-Functions allow you to turn code into modules and improves script organisation
-Example with hello world as the function:
-hello_world() {
-    echo “
-}
-hello_world
-./script.sh
-Hello World! (outcome of running script)
-Example with greet person as function:
-greet_person() {
-    local name=””
-    Echo “
-}
-greet_person “Ahmed”
-./script.sh
-Hello, Ahmed! (outcome of running script)

Function Parameters –

-Allows you to pass data to functions to enable them to perform specific tasks based on specific inputs
-There’s two types: Positional and Special parameters, example:
-print_args() {
-  echo “Script name: -bash” (-bash and  are special parameters)
-  echo “First argument: ” ( and  are positional parameters)
-  echo “Second argument: ”
-  echo “All arguments: ” 
-}
-Print_args “Alice” “Bob” “Ahmed”
-./script.sh
-Number of arguments: 3 First argument: Alice Second argument: Bob All arguments: Alice Bob Ahmed (outcome of running script)

User inputs –

-Allows our script to interact with users to make them more dynamic and interactive
-The read command captures the user input, example:
-greet_user() {
-   echo “What is your name?”
-   read name
-   echo “
-}
-greet_user
-./script.sh
-What is your name?
-Faiz (Terminal will be trailing unless you type the user name)
-Hello, Faiz!

Handling bad data –

-Refers to unexpected errors or undesigned behaviour in the script
-Provides feedback to users
-Input sanitisation is a good method to handle bad data, it does it by removing and cleaning the data
-Conditional statements can be used to validate user inputs to ensure they meet criteria.

