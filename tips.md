# Tips: Git, PowerShell, etc.

# Git
** Bash find latest commits authors (branch owner) to all branches **
```bash
git for-each-ref --format='%(committerdate) %09 %(authorname) %09 %(refname)' | sort -k5n -k2M -k3n -k4n
```
** List commiters' emails which are not (grep -v) example.com **
```bash
git log --after='2018-12-01 00:00:00' | grep Author: | grep -v @example.com | sort | uniq -c | sort -n -r
```
** Compare two branches. Find all commits at Right branch which are new for Left branch. Do not include Left's commits even if they are new for Right **
```bash
git diff origin/master...origin/feature_branch > /D/diff.patch
```

** Rewrite commit messages **
- The way with intective rebase [Changing a commit message](https://help.github.com/articles/changing-a-commit-message/) see section "Amending the message of older or multiple commit messages"
- Another way with bash [Update git commit messages](https://davidwalsh.name/update-git-commit-messages)
```bash
git filter-branch --msg-filter 'echo "bug ###### - \c" && cat' master..HEAD
```

# Nuget
Get unique sorted list of packages in solution
```powershell
#Execute in Powershell or Visual Studio "Package Manager Console"
Get-Package | select -expand Id | Sort-Object -Unique > D:\packages.txt
```
