Change PATH Permanently -
-	The path environmental variable is a critical system variable that specifies the directories where the shell should look for executable files
-	Sometimes we might need to add out own directories to path, particularly when installing new software or when we want our own binaries to be available system-wide
-	mkdir my_scripts
-	vi my_scripts/hello_world.sh
-	#!/bin/bash
-	echo “Hello World”
-	chmod +x my_scripts/hello_world.sh
-	echo “export PATH=$PATH:~/my_scripts” >> ~/.zshrc (Adds the directory to the path)
-	source ~/.zshrc
-	Hello_world.sh
-	Hello World (Outcome)
-	cd Desktop
-	Desktop hello_world.sh
-	Hello World (Outcome)

Reading Environment Variables –

-	Understanding how to work with environment variables can greatly enhance your scripting capabilities.
-	They are like container that hold valuable information for scripts
-	They provide a way to store settings and configurations that our scripts can access when needed
-	#!/bin/bash
-	echo “Home Directory: $HOME”
-	echo “Current user: $USER”
-	./script.sh
-	Home Directory: /Users/Faiz Current user: Faiz (Outcome of running script)

Standard Environment Variables –

-	Gives us valuable insights into various aspects of the system, user and runtime environment
-	Provides information that can help us create more robust and adaptable bash scripts
-	#!/bin/bash
-	echo “Executable Paths: $PATH”
-	echo “Default Language: $LANG”
-	./script.sh
-	(Displays the paths of the system and the language used when running the script)

Reading Files –

-	Allows us to access and extract valuable information from various types of files
-	#!/bin/bash
-	read_file() {
-	      local file_path=”$1”
-	      while IFS=read -r line; do 
-	            echo “$line”
-	      done < “$file_path”
-	}
-	read_file “./log.txt”
-	./script.sh
-	(Outcome of running the script is that it prints each line of the file)

Writing Files –

-	Allows us to create, modify and store information in various formats within bash
-	#!/bin/bash
-	write_to_file() {
-	     local file_path=”$1”
-	     local data=”$2”
-	     echo “$data” > “$file”
-	}
-	write_to_file “read.txt” “Hello World”
-	./script.sh (running the script wont display anything)
-	cat read.txt
-	Hello World (Outcome of writing file in bash)
<img width="936" height="1290" alt="image" src="https://github.com/user-attachments/assets/4e73a02a-7868-49c2-a8ee-45c792eaaa07" />
