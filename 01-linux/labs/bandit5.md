#Bandit level 5 -> 6
Solution & Explanation - 
‘ls’ to list the contents
‘cd inhere/‘ to enter the directory
‘ls’ list the contents in the directory
‘find . -type f -size 1033c ! -executable -exec file {} \; | grep text’ this find command searches for 1033 byte files, excludes executable files, runs ‘file’ command on each result and filters for human-readable files
Password - HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
What I learned - the find command can be used to filter out files 