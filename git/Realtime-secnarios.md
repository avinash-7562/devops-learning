
--> for cloning the repo no need of git authentication

updating user email and name
===============================
$ git push
remote: Permission to avinash-7562/devops-learning.git denied to girijanulu18.
fatal: unable to access 'https://github.com/avinash-7562/devops-learning.git/': The requested URL returned error: 403

go to windows credentials in credential manager and delete git url

rij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$ git config --list
---------
user.email=girijanulu@gmail.com
user.name=girijanulu18
---------

girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$

girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$ git push
info: please complete authentication in your browser...
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (5/5), 879 bytes | 879.00 KiB/s, done.
Total 5 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/avinash-7562/devops-learning.git
   58b274f..20c20c7  main -> main


girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$ git config --list
------------------
user.email=girijanulu@gmail.com
user.name=girijanulu18
----------------

girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$ git config --global user.name "avinash-7562"

girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$ git config --global user.email "avinashnulu98@gmail.com"

girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$ git config --list
--------------------
user.email=avinashnulu98@gmail.com
user.name=avinash-7562
---------------------

empty commit to check user got updated in github:
==================================================
girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$ git commit -m "empty_commit"
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$ git push
Everything up-to-date

girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$ git commit --allow-empty -m "empty_commit"
[main b714882] empty_commit

girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$ git push
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 187 bytes | 187.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/avinash-7562/devops-learning.git
   20c20c7..b714882  main -> main

girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$

renaming repo name:
====================
1. rename the repo in github by directly going to settings in repo
2. in the local execute below commands
   $ git remote set-url origin https://github.com/avinash-7562/devsecops-learning.git

   $ git remote -v
   origin  https://github.com/avinash-7562/devsecops-learning.git (fetch)
   origin  https://github.com/avinash-7562/devsecops-learning.git (push)

   $ git push
   Everything up-to-date

3. the reponame will not be updated in local even git pull wont work manually change name using mv command
   note : reponame cannot be renamed if that is opened by any editor