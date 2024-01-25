---
title: Troubleshooting and FAQ
layout: home
nav_order: 7
---



# Other

### Removing file and folder from Github Repository only

Remove file from Github repository only 

     git rm --cached file1.txt file2.txt

Remove folder from Github repository only 

     git rm -r --cached folder_name

Then

     git commit -m "Remove folder from Git repository"
     git push origin <branch-name>
