#Bandit level 6 -> 7
Solution & Explanation - 
‘whoami’ displays what user I am
‘find / -user bandit7 -group bandit6 -size 33c 2>/dev/null’ this filters out and shows files owned by user bandit7, owned by group bandit6, file size of 33 bytes and hides permission denied by errors
‘cat /var/lib/dpkg/info/bandit7.password’ displays the text in the file
Password - morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
What I learned - that the find command can be used to filter out files owned by users and groups