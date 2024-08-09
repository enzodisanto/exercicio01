
Configuração Inicial
---

```bash
enzodisanto@Enzos-MacBook-Pro ~/D/i/github> pwd
/Users/enzodisanto/Documents/impacta/github
enzodisanto@Enzos-MacBook-Pro ~/D/i/github> mkdir exercicio01
enzodisanto@Enzos-MacBook-Pro ~/D/i/github> cd exercicio01/
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01> git config --global user.name "Enzo Di Santo"
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01> git config --global user.email "enzoddisanto@gmail.com"                                     
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01> git init 
Initialized empty Git repository in /Users/enzodisanto/Documents/impacta/github/exercicio01/.git/
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> ls -la
total 0
drwxr-xr-x  3 enzodisanto  staff   96 Aug  9 17:40 ./
drwxr-xr-x  3 enzodisanto  staff   96 Aug  9 17:39 ../
drwxr-xr-x  9 enzodisanto  staff  288 Aug  9 17:40 .git/
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> ls -la .git/
total 24
drwxr-xr-x   9 enzodisanto  staff  288 Aug  9 17:40 ./
drwxr-xr-x   3 enzodisanto  staff   96 Aug  9 17:40 ../
-rw-r--r--   1 enzodisanto  staff   21 Aug  9 17:40 HEAD
-rw-r--r--   1 enzodisanto  staff  137 Aug  9 17:40 config
-rw-r--r--   1 enzodisanto  staff   73 Aug  9 17:40 description
drwxr-xr-x  15 enzodisanto  staff  480 Aug  9 17:40 hooks/
drwxr-xr-x   3 enzodisanto  staff   96 Aug  9 17:40 info/
drwxr-xr-x   4 enzodisanto  staff  128 Aug  9 17:40 objects/
drwxr-xr-x   4 enzodisanto  staff  128 Aug  9 17:40 refs/
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> date
Fri Aug  9 17:41:14 -03 2024
```

###

Atvidade
---

```bash
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> ls -l
total 0
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> echo 01 > arquivo.txt
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> ls -l
total 8
-rw-r--r--  1 enzodisanto  staff  3 Aug  9 17:44 arquivo.txt
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> git add .
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   arquivo.txt

enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> git commit -m "Add arquivo txt"
[main (root-commit) 91b6ad5] Add arquivo txt
 1 file changed, 1 insertion(+)
 create mode 100644 arquivo.txt
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> git status
On branch main
nothing to commit, working tree clean
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> 
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> 
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> echo 02 > arquivo.txt 
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> git diff
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> git add .
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   arquivo.txt

enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> git diff
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> echo 03 > arquivo.txt 
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> git diff 
diff --git a/arquivo.txt b/arquivo.txt
index 9e22bcb..75016ea 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-02
+03
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> git restore .
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> git status 
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   arquivo.txt

enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> git commit -m "Primeiro Commit | Exercicio 01"
[main ddaaf47] Primeiro Commit | Exercicio 01
 1 file changed, 1 insertion(+), 1 deletion(-)
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> git log 
commit ddaaf47b8ffe9b1d204c84d7976c1781530f0434 (HEAD -> main)
Author: Enzo Di Santo <enzoddisanto@gmail.com>
Date:   Fri Aug 9 17:48:53 2024 -0300

    Primeiro Commit | Exercicio 01

commit 91b6ad5605b5953a1aca933aa10812ee670c76fa
Author: Enzo Di Santo <enzoddisanto@gmail.com>
Date:   Fri Aug 9 17:45:28 2024 -0300

    Add arquivo txt
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> 
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> echo "*.txt" >.gitignore
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> cat .gitignore 
*.txt
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> echo > novo.txt 
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
	.gitignore
enzodisanto@Enzos-MacBook-Pro ~/D/i/g/exercicio01 (main)> date
Fri Aug  9 18:08:48 -03 2024    
```