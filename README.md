# XML_GIT_Homework_1
## 1. Create an external repository called XML_GIT on Github site.
I go to https://github.com/MariaDash, click "Repositories", click "New", make it Public, add README.md file, create repository.
## 2. Clone repository to local PC
I go to repository page--> Code --> Local and copy its link. And here two options: 
You can copy by HTTPS (unsecure without password) or SSH (need specific configuration and it is secure and always ask password).. I cpoy via HTTPS.
On PC I go to my folder "XML", right click "Gitbash Here" and open a terminal Gitbash in this folder.
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML (main)
$ git remote set-url origin https://github.com/MariaDash/XML_GIT.git

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML (main)
$ git remote -v
origin  https://github.com/MariaDash/XML_GIT.git (fetch)
origin  https://github.com/MariaDash/XML_GIT.git (push)

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML (main)
$ git clone https://github.com/MariaDash/XML_GIT.git
Cloning into 'XML_GIT'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML (main)
$ ls
XML_GIT/

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML (main)
$ ls XML_GIT/
README.md

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML (main)
$
```
## 3. Inside the local XML, create a “new.xml” file.
```
 Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ touch new.xml

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$
```
## 4. Add a file for tracking
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ git add new.xml

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   new.xml


Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$
```
## 5. Do commit it.
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ git commit -m "creating new.xml"
[main 6ed971d] creating new.xml
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 new.xml

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ 
```
## 6. Send the file to remote repository
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 277 bytes | 138.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/MariaDash/XML_GIT.git
   ea8eb0a..6ed971d  main -> main

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$
```
## 7. Edit the content of the “new.xml” file - write information about yourself (name, age, number of pets, future desired salary). Everything is written in XML format.
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ vim new.xml

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ cat new.xml
<?xml version="1.0" encoding="UTF-8"?>
<info>
        <name>Mariia</name>
        <surname>Dashkova</surname>
        <age>35</age>
        <pets>0</pets>
        <salary>1500</salary>



</info>

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$
```
## 8. Send chandes to remote repository
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   new.xml

no changes added to commit (use "git add" and/or "git commit -a")

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ git commit -am "changes in new.xml"
warning: in the working copy of 'new.xml', LF will be replaced by CRLF the next time Git touches it
[main 402e148] changes in new.xml
 1 file changed, 11 insertions(+)

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 403 bytes | 134.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/MariaDash/XML_GIT.git
   6ed971d..402e148  main -> main

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$
```
## 9. Create preferences.xml file
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ touch preferences.xml

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ ls
README.md  new.xml  preferences.xml

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$
```
## 10. In the preferences.xml file, add information about your preferences (Favorite movie, favorite series, favorite food, favorite season, side you would like to visit) in XML format.
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ vim preferences.xml

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ cat preferences.xml
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ vim preferences.xml

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ cat preferences.xml
<?xml version="1.0" encoding="UTF-8"?>
<preferences>
        <favMovie>G.I.Jane</favMovie>
        <favTVShow>Friends</favTVShow>
        <favFood>Wok</favFood>
        <favSeason>winter</favSeason>
        <countryToTravel>Italy</countryToTravel>


</preferences>


Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$

```
## 11. Create a sklls.xml file add information about the skills that will be studied in the course in XML format.
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ vim skills.xml

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ cat skills.xml
<?xml version="1.0" encoding="UTF-8"?>
<skills>
        <value1>SQL</value1>
        <value2>Postman</value2>
        <value3>GIT</value3>
        <value4>Terminal</value4>
        <value5>DevTools</value5>
        <value6>Jmeter</value6>
        <value7>Fiddler</value7>
        <value8>Charles Proxy</value8>
        <value9>ADB</value9>
</skills>

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$
```
## 12. Do one string commit.
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ git add .
warning: in the working copy of 'preferences.xml', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of 'skills.xml', LF will be replaced by CRLF the next time Git touches it

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   git
        new file:   preferences.xml
        new file:   skills.xml


Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ git commit -m "add skills.xml and preferences.xml"
[main e1d233c] add skills.xml and preferences.xml
 3 files changed, 23 insertions(+)
 create mode 100644 git
 create mode 100644 preferences.xml
 create mode 100644 skills.xml

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$
```
## 13. Send 2 files at once to an external repository.
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ git push
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (5/5), 713 bytes | 178.00 KiB/s, done.
Total 5 (delta 0), reused 0 (delta 0), pack-reused 0
remote: This repository moved. Please use the new location:
remote:   https://github.com/MariaDash/XML.git
To https://github.com/MariaDash/XML_GIT.git
   402e148..e1d233c  main -> main

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$
```

## 14. Create a bug_report.xml file on the web interface.
## 15. Make Commit changes (save) changes on the web interface.
## 16. Modify the bug_report.xml file on the web interface, add a bug report in XML format.
## 17. Make Commit changes (save) changes on the web interface.
## 18. Synchronize external and local XML repository
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ git pull
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (7/7), done.
remote: Total 8 (delta 3), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (8/8), 1.85 KiB | 65.00 KiB/s, done.
From https://github.com/MariaDash/XML_GIT
   e1d233c..4b09b5b  main       -> origin/main
Updating e1d233c..4b09b5b
Fast-forward
 bug_report.xml | 5 +++++
 git            | 0
 2 files changed, 5 insertions(+)
 create mode 100644 bug_report.xml
 delete mode 100644 git

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$ ls
README.md  bug_report.xml  new.xml  preferences.xml  skills.xml

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/XML_GIT (main)
$
```

