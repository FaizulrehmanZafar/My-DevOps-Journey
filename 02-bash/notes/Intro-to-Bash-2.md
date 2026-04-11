Writing a script –

-touch my-first-script.sh 
-vi my-first-script.sh (this will open the script and will look like the vim command interface)
-echo “
-:wq! (this saves the script and returns to normal terminal)
-chmod +x my-first-script.sh (this chmods the script)
-./my-first-script.sh (this executes the script)
-Hello World! (this is the outcome of executing the script)

Running scripts from anywhere –

-You can do so by placing the script in of our path environmental variables
-echo /usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin (this shows the paths you can move it to)
-sudo mv my-first-script.sh /usr/local/bin/my-first-script
-(will then ask for password)
-sudo chmod +x /usr/local/bin/my-first-script
-(Now you can run the script without using ‘.sh’ at the end from any directory’)

