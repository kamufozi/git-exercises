# GIT ADVANCED EXERCISES

## Part 1
 
### Challenge 1
```sh
Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git
$ touch test{1..4}.md
git add test1.md && git commit -m "chore: Create initial file"
git add test2.md && git commit -m "chore: Create another file"
git add test3.md && git commit -m "chore: Create third and fourth files"
fatal: not a git repository (or any of the parent directories): .git
fatal: not a git repository (or any of the parent directories): .git
fatal: not a git repository (or any of the parent directories): .git

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git
$ git init
Initialized empty Git repository in C:/Users/Fozi Chris/OneDrive/Desktop/git/.git/

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (master)
$ git add test1.md && git commit -m "chore: Create initial file"
git add test2.md && git commit -m "chore: Create another file"
git add test3.md && git commit -m "chore: Create third and fourth files"
[master (root-commit) 8620b8e] chore: Create initial file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test1.md
[master 3085d76] chore: Create another file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md
[master a1da5b3] chore: Create third and fourth files
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (master)
$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test4.md

nothing added to commit but untracked files present (use "git add" to track)

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (master)
$ git log --oneline
a1da5b3 (HEAD -> master) chore: Create third and fourth files
3085d76 chore: Create another file
8620b8e chore: Create initial file

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (master)
$ git add test4.md

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (master)
$ git commit -m 'Added the test 4 file'
[master c392fb4] Added the test 4 file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test4.md
 ```
### challenge 2

 ```sh
Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (main)
$ git log --oneline
34e7879 (HEAD -> main, origin/main) Changed the readme file
c392fb4 Added the test 4 file
a1da5b3 chore: Create third and fourth files
3085d76 chore: Create another file
8620b8e chore: Create initial file

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (main)
$ git rebase HEAD~N
fatal: invalid upstream 'HEAD~N'

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (main)
$ git rebase -i HEAD~N
fatal: invalid upstream 'HEAD~N'

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (main)
$ git rebase -i HEAD~5
fatal: invalid upstream 'HEAD~5'

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (main)
$ git rebase -i HEAD ~ 1
usage: git rebase [-i] [options] [--exec <cmd>] [--onto <newbase> | --keep-base] [<upstream> [<branch>]]
   or: git rebase [-i] [options] [--exec <cmd>] [--onto <newbase>] --root [<branch>]
   or: git rebase --continue | --abort | --skip | --edit-todo

    --[no-]onto <revision>
                          rebase onto given branch instead of upstream
    --[no-]keep-base      use the merge-base of upstream and branch as the current base
    --no-verify           allow pre-rebase hook to run
    --verify              opposite of --no-verify
    -q, --[no-]quiet      be quiet. implies --no-stat
    -v, --[no-]verbose    display a diffstat of what changed upstream
    -n, --no-stat         do not show diffstat of what changed upstream
    --stat                opposite of --no-stat
    --[no-]signoff        add a Signed-off-by trailer to each commit
    --[no-]committer-date-is-author-date
                          make committer date match author date
    --[no-]reset-author-date
                          ignore author date and use current date
    -C <n>                passed to 'git apply'
    --[no-]ignore-whitespace
                          ignore changes in whitespace
    --[no-]whitespace <action>
                          passed to 'git apply'
    -f, --[no-]force-rebase
                          cherry-pick all commits, even if unchanged
    --no-ff               cherry-pick all commits, even if unchanged
    --ff                  opposite of --no-ff
    --continue            continue
    --skip                skip current patch and continue
    --abort               abort and check out the original branch
    --quit                abort but keep HEAD where it is
    --edit-todo           edit the todo list during an interactive rebase
    --show-current-patch  show the patch file being applied or merged
    --apply               use apply strategies to rebase
    -m, --merge           use merging strategies to rebase
    -i, --interactive     let the user edit the list of commits to rebase
    --[no-]rerere-autoupdate
                          update the index with reused conflict resolution if possible
    --empty (drop|keep|ask)
                          how to handle commits that become empty
    --[no-]autosquash     move commits that begin with squash!/fixup! under -i
    --[no-]update-refs    update branches that point to commits that are being rebased
    -S, --[no-]gpg-sign[=<key-id>]
                          GPG-sign commits
    --[no-]autostash      automatically stash/stash pop before and after
    -x, --[no-]exec <exec>
                          add exec lines after each commit of the editable list
    -r, --[no-]rebase-merges[=<mode>]
                          try to rebase merges instead of skipping them
    --[no-]fork-point     use 'merge-base --fork-point' to refine upstream
    -s, --[no-]strategy <strategy>
                          use the given merge strategy
    -X, --[no-]strategy-option <option>
                          pass the argument through to the merge strategy
    --[no-]root           rebase all reachable commits up to the root(s)
    --[no-]reschedule-failed-exec
                          automatically re-schedule any `exec` that fails
    --[no-]reapply-cherry-picks
                          apply all changes, even those already present upstream


Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (main)
$ git rebase -i HEAD~1
Successfully rebased and updated refs/heads/main.
Deletion of directory '.git/rebase-merge' failed. Should I try again? (y/n) y
Deletion of directory '.git/rebase-merge' failed. Should I try again? (y/n) y
Deletion of directory '.git/rebase-merge' failed. Should I try again? (y/n) n
error: could not remove '.git/rebase-merge'

reword 3085d76 chore: Create another file
chore: Create second file
Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (|REBASE)
$ rm -rf .git/rebase-merge

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (main)
$ git log --oneline
34e7879 (HEAD -> main, origin/main) Changed the readme file
c392fb4 Added the test 4 file
a1da5b3 chore: Create third and fourth files
3085d76 chore: Create another file
8620b8e chore: Create initial file

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (main)
$ git rebase -i HEAD~4
[detached HEAD ab1f6cb] chore: Create second file
 Date: Wed Mar 5 13:34:50 2025 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md
Successfully rebased and updated refs/heads/main.
Deletion of directory '.git/rebase-merge' failed. Should I try again? (y/n) y
Deletion of directory '.git/rebase-merge' failed. Should I try again? (y/n) y
Deletion of directory '.git/rebase-merge' failed. Should I try again? (y/n) n
error: could not remove '.git/rebase-merge'

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (|REBASE)
$ git log --oneline
90b847f (HEAD -> main) Changed the readme file
77a0d68 Added the test 4 file
1a9818d chore: Create third and fourth files
ab1f6cb chore: Create second file
8620b8e chore: Create initial file

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (|REBASE)
$ rm -rf .git/rebase-merge

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (main)
$ git status
On branch main
Your branch and 'origin/main' have diverged,
and have 4 and 4 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)

nothing to commit, working tree clean

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (main)
$ git pull
Merge made by the 'ort' strategy.

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (main)
$ git pull -f
Already up to date.
 ```
OUTPUT :
 Before : $ `git log --oneline`
 ```sh
34e7879 (HEAD -> main, origin/main) Changed the readme file
c392fb4 Added the test 4 file
a1da5b3 chore: Create third and fourth files
3085d76 chore: Create another file
8620b8e chore: Create initial file
After : $ git log --oneline
90b847f (HEAD -> main) Changed the readme file
77a0d68 Added the test 4 file
1a9818d chore: Create third and fourth files
ab1f6cb chore: Create second file
8620b8e chore: Create initial file
```
### challenge 3
```sh
Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (main)
before:Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git ((90b847f...)|CHERRY-PICKING)
$ git log --oneline
90b847f (HEAD) Changed the readme file
77a0d68 Added the test 4 file
1a9818d chore: Create third and fourth files
ab1f6cb chore: Create second file
8620b8e chore: Create initial file
$ git rebase -i HEAD~2
After : Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (main|REBASE 4/5)
$ git log --oneline
934bb38 (HEAD) Combining two commits
77a0d68 Added the test 4 file
1a9818d chore: Create third and fourth files
ab1f6cb chore: Create second file
8620b8e chore: Create initial file
```
Challenge 4

```sh
Before reset : 
Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (main)
$ git log --oneline
c2fc6a6 (HEAD -> main, origin/main) Edited the readme file and added the third challenge
66e48be Finished the 2nd challenge
168b261 Merge branch 'main' of https://github.com/kamufozi/git-exercises
90b847f Changed the readme file
77a0d68 Added the test 4 file
1a9818d chore: Create third and fourth files
ab1f6cb chore: Create second file
34e7879 Changed the readme file
c392fb4 Added the test 4 file
8620b8e chore: Create initial file
a1da5b3 chore: Create third and fourth files
3085d76 chore: Create another file

After reset :
Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (main)
$  git reset --soft HEAD~6

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (main)
$ git add third_file.txt
git commit -m "Create Third File"
fatal: pathspec 'third_file.txt' did not match any files
[main 1280a38] Create Third File
 3 files changed, 237 insertions(+)
 create mode 100644 readme.md
 create mode 100644 test3.md
 create mode 100644 test4.md

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (main)
$ git push -f
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 2.58 KiB | 659.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/kamufozi/git-exercises.git
 + c2fc6a6...1280a38 main -> main (forced update)

Fozi Chris@DESKTOP-EI6IC2P MINGW64 ~/OneDrive/Desktop/git (main)
$ git log --oneline
1280a38 (HEAD -> main, origin/main) Create Third File
ab1f6cb chore: Create second file
8620b8e chore: Create initial file
##When we push and you go miles back on your commit and you reset and change the name 
##The files will come also edited with that name 