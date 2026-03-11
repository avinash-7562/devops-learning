
1. for cloning the repo no need of git authentication

$ git clone https://github.com/avinash-7562/devops-learning.git
Cloning into 'devops-learning'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)


$ git push
remote: Permission to avinash-7562/devops-learning.git denied to girijanulu18.
fatal: unable to access 'https://github.com/avinash-7562/devops-learning.git/': The requested URL returned error: 403

go to windows credentials in credential manager and delete git url

rij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$ git config --list
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=C:/Program Files/Git/mingw64/etc/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=false
pull.rebase=false
credential.helper=manager
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=main
user.email=girijanulu@gmail.com
user.name=girijanulu18
core.repositoryformatversion=0
core.filemode=false
core.bare=false
core.logallrefupdates=true
core.symlinks=false
core.ignorecase=true
remote.origin.url=https://github.com/avinash-7562/devops-learning.git
remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
branch.main.remote=origin
branch.main.merge=refs/heads/main

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
$

girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$

girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$ git config --list
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=C:/Program Files/Git/mingw64/etc/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=false
pull.rebase=false
credential.helper=manager
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=main
user.email=girijanulu@gmail.com
user.name=girijanulu18
core.repositoryformatversion=0
core.filemode=false
core.bare=false
core.logallrefupdates=true
core.symlinks=false
core.ignorecase=true
remote.origin.url=https://github.com/avinash-7562/devops-learning.git
remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
branch.main.remote=origin
branch.main.merge=refs/heads/main

girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$


girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$

girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$ ^C

girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$ git config --global user.name "avinash-7562"

girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$ git config --global user.email "avinashnulu98@gmail.com"

girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$

girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$

girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$ git config --list
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=C:/Program Files/Git/mingw64/etc/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=false
pull.rebase=false
credential.helper=manager
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=main
user.email=avinashnulu98@gmail.com
user.name=avinash-7562
core.repositoryformatversion=0
core.filemode=false
core.bare=false
core.logallrefupdates=true
core.symlinks=false
core.ignorecase=true
remote.origin.url=https://github.com/avinash-7562/devops-learning.git
remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
branch.main.remote=origin
branch.main.merge=refs/heads/main

girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$


girij@Girija_Nulu MINGW64 ~/avinash_devops/devops-learning (main)
$

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


