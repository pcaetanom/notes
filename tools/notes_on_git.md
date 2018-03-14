
#### Key concepts:

&rarr; **DVCS** - Distributed Version Control System  
* "A peer-to-peer approach to Version Control.." "... No canonical, reference copy of the codebase exists by default; only working copies.  

&rarr; **master**
* stem of branch tree 

&rarr; **HEAD** 
* a pointer to the current branch that your <working-directory> is pointing to. HEAD can point to Master or to any other branch in the project tree.
    Although not entirely correct we can think of this as your remote git application manages version control of your project in a location : $origin/$HEAD

&rarr; **origin**
* An alias for the project's <working-directory> in a remote location
* git config default is that 'push' is 'local', use --set-upstream argument (or -u) 
    when pushing a branch or master changes from local to a remote 'origin'
 
&rarr; **staging area** 
* An index of file changes in our current (local) work. These changes will take effect (in the branch your HEAD points to) only after you have 'committed' the changes indexed in your staging area (commit)
commit: a change or set of changes moved from staging area to HEAD branch.

&rarr; **blob** 
* Any file changes within a tracked folder are referred to as a 'blob'. Blobs are organised in a tree system 
    within git's filesystem. Each blob is assigned a unique 'SHA'. This hash SHA allows us reference a specific object "blob" (i.e. a specific file change)

&rarr; **push**
* 'pushes' the branch changes implemented in your local machine, to another location (usually origin)

&rarr; **fetch**
* 'fetches' branch changes implemented from the branch's 'origin'

&rarr; **merge**
* Merge changes from another branch on the current branch, ideally fast-forward but can be done recursive


#### Quick reference
##### (AKA cmds I use 99.9% of the time)

###### config
    
    # (my *nix preference)
    git config --global core.editor "<emacs_path>"
    # (my Windows preference)
    git config --global core.editor "<notepadPlusPlus>/notepad++.exe -multiInst -nosession"


    git config --local user.name "username" # user for server login  
    git config credential.https://example.com.myusername myusername # e.g. github repo
    git config --local credential.helper wincred # Win only - for server access with windows login
    
    

###### local
    git init # creates a new (empty) Git repository.  
    git status #(inspects the contents of the working directory and staging area)
    git add <filename> #(adds files from the working directory to the staging area)
    git diff # shows diff between working directory and the staging area)
    git commit -m "This is a descriptive note that will be displayed in log, explaining the change implemented by this commit" 
    git commit --amend # edit last commit msg
    git add <left_out_file> & git commit --amend --no-edit # adds missing file to previous commit without msg
    git show <SHA> # shows a diff for the blob of code in a specific commit 
    git log # shows a list of all previous commits




# Copy Pasta dump below:

backtracking in Git
    cd into your <working-directory>
    
        git checkout HEAD <filename> #(reverts <filename> changes in the working directory to match 
                                                                        the <filename> in  the HEAD.
                
        # [HEAD] is a pointer to the current branch that the <working-directory> is in.
    
        git reset HEAD <filename> # Unstages file changes in the staging area (file changes prior to commit).    
        
        git reset <SHA> # resets back to a specific commit history, with the unique hash <SHA>

        git revert <SHA> # reverts a single commit in commit history, with the unique hash <SHA>
        
        git checkout <SHA> updates working directory to match some point in branch dev
            resolving a detached head with git checkout:
            git commit -m "....."
            git branch my-temporary-work
            git checkout master
            git merge my-temporary-work
            
        git rm -r --cached <file> clears all stage data regarding <file>
        
    safe revert :
        git revert --no-commit HEAD~<N+1> Number of commits back from head
        git commit
        git revert --no-commit HEAD~3..HEAD


Git branching

    cd into your <working-directory>
    
        git branch -v # Lists all local branches.
        git branch -r # lists all remote branches
        git remote show origin # Lists all branches tracked on remote

        git branch <branch_name> # Creates a new branch.
    
        git checkout <branch_name> # Used to switch 'into' another branch in the same project.
    
        git merge <branch_name> # Used to join file changes from branch to master.
    
        git merge --abort # revert the merge process, if there is any conflict in finding a 'common ancestor' path in the previous merge cmd.  
        git branch -d <branch_name> # Deletes the branch <branch_name> 
    
    clean merge to master
        (on branch directory)
        git checkout master
        git pull origin master
        git merge origin/<branch_to_merge>
        git push -u origin master
        
    merge conflicts
        git checkout --ours <file>
        git checkout --theirs <file>
        git fetch origin # update local awareness of remote branch updates

GIT clone workflow

     basic git local clone from a remote
        git clone <remote-location>
        git checkout <relevant-branch-name-within-repo>
     clone a specific branch
        git clone -b <branch> <remote_repo>  

Git remote workflow.

    cd into your <working-directory>
    
    
        git config --global user.name "username" # required for server login, git will log you in with a password prompt 
                    git config credential.https://example.com.username myusername
        git config credential.https://github.com/PCaetanoRenishaw PCaetanoRenishaw
        git config --local credential.helper wincred
            # using the username setup in this git config.
    
        # # Creates a local copy of an already egixisting remote repo. 
    
        git remote -v # Lists a Git project's existing remotes
    
        git fetch # Fetches work from the remote into the local copy (i.e. changes made my others)
    
        git origin/master (merges remote master int o your local branch).
    
        git push -u origin <local-branch> # Pushes a local branch (master or other) to the origin in remote 
                    
            # N.B. argument "-u" as "--set-upstream" to make it clear that the origin is in remote 
            # and not in local origin/<local-branch>.

    
        git remote add origin <remote-location> # copy local repo into remote location
                        
            # e.g. "https://username@validserverurl/file.git" 


advanced
 update password
    
    

 change default text editor for commit/merge messages
    git config --global core.editor "<editorOfYourChoice>"  (e.g. git config --global core.editor "notepad") 
    
  
 index a Local branch to be mapped to an already existing remote branch
    git clone remote
    git branch <myLocalBranchWithSameNameAsRemoteBranch>
    git checkout <myLocalBranchWithSameNameAsRemoteBranch> 
    git branch --set-upstream-to=origin/<branch> myLocalBranchWithSameNameAsRemoteBranch 
    git pull
    
 rebase squash "micro-commits"
    git rebase -i <SHA-of-Commit N-1> from where we want to squash
    change push commits to 'squash'
    edit commmit message for group of squashed commits
    git push origin +<branch>

 edit last commit
    git commit --amend

remove unstaged files
    git clean -n  : dry run shows what would happen
    git clear -i  : remove items but with prompt
    git clean -df  : directories as well and force gitignore
    git checkout -- .
    git clean removes all untracked files (warning: while it won't delete ignored files mentioned directly in .gitignore, it may delete ignored files residing in folders) and git checkout clears all unstaged changes.

merge cherrypicked commits
    git checkout master 
    git cherry-pick < commit-id of newbranch's 4th commit >
    
cherry-pick from file diffs
    (bash) find specific file paths
    find . -name foo.cs -printf '%h%f\n'
    git show SHA -- file1.txt file2.txt | git apply -
    
reset project to take in gitignore
    **First commit your current changes or you will lose them.
    git rm . -r --cached
    git add .
    git commit -m "fixed untracked files"

 force add files despite gitignore exemptions
    git add --force path/fileThatShouldBeIgnored.foo

force add all files of file extension type *.foo        
    git add path/\*.txt    (will add all files in path sub-directories)
    
 use shared network drive as remote
 in remote location
    git init --bare <remote-location>
 in local
    git init 
    git remote add origin <remote-location>
    same as before add -> commit -> push -u origin master
  
 manage remote 
 git remote -v
 git remote add origin <remote-location>
 git remote rm origin <remote-location> 
 
 (use only hunks of diff rather than the whole file)
 git add -p <file> (patching)
 git add --patch <file> 
    note -p is a shortcut to "patch" which is actully part of interactive mode ( -i )
    keyboard shortcuts:
    y stage this hunk for the next commit
    n do not stage this hunk for the next commit
    q quit; do not stage this hunk or any of the remaining hunks
    a stage this hunk and all later hunks in the file
    d do not stage this hunk or any of the later hunks in the file
    g select a hunk to go to
    / search for a hunk matching the given regex
    j leave this hunk undecided, see next undecided hunk
    J leave this hunk undecided, see next hunk
    k leave this hunk undecided, see previous undecided hunk
    K leave this hunk undecided, see previous hunk
    s split the current hunk into smaller hunks
    e manually edit the current hunk
    ? print hunk help
 find diff between HEAD and commit in git log   
 git whatchanged -m -n 1 -p <commit hash value>
 
 
 tags
    git tag -a <tag_content> <sha> -m "tooltip message"
    git push --tags origin <branch>
    
 git config
 $ git config --global --list
 $ git config --local --list
 $ git config --local <some-valid-field> "field-value"
 
 stash
 
 git add . & git stash  save working dir state
 
 git stash list                             # list stash entries
 git stash show -p stash@{<N_stash_index>}  # diff stash
 git stash apply stash@{<N_stash_index>}    # applies stash
 git stash pop                              # applies first stash entry pop's from stash stack 


using github via a proxy (on windows)
[http]
	proxy = http://some_local_host_proxy_address.0.0.1:9000
    sslCAInfo = C:/Users/username/local_copy_of_proxy_certificate.cer

when local config is required before cloning 
(track already existing remote)

git init
(change local config as required)
git remote add origin
git pull origin master