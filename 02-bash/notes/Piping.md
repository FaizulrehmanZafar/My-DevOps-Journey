Piping –

-Allows you to pass the output of one command as an input to another, example:
#!/bin/bash
-get_file_count() {
-    local directory=”$1”
-    Local file_count
-File_count=$(ls"$directory")
-}
-get_file_count “./”
-./script.sh
-(Outcome of running the script gives you the number of files in the directory you’re in)
