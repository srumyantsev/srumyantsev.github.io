# If something went wrong
* (FAQ) [Flight rules for Git](https://github.com/k88hudson/git-flight-rules/blob/master/README.md)

# Tips
* Difference between two and three dots in diff and log commands
  * [What are the differences between double-dot “..” and triple-dot “…” in Git commit ranges?](https://stackoverflow.com/questions/462974/what-are-the-differences-between-double-dot-and-triple-dot-in-git-com)
  * [What are the differences between double-dot “..” and triple-dot “…” in Git diff commit ranges?](https://stackoverflow.com/questions/7251477/what-are-the-differences-between-double-dot-and-triple-dot-in-git-dif)

# Git rebasing
* (Article) [Git rebase and the golden rule explained.](https://medium.freecodecamp.org/git-rebase-and-the-golden-rule-explained-70715eccc372)
* (Article) [Git Rebasing Public Branches Works Much Better Than You’d Think](https://redfin.engineering/git-rebasing-public-branches-works-much-better-than-youd-think-ecc9a115aea9)

# Git internals
* (Article) [Git Internals - Git Objects](https://git-scm.com/book/en/v2/Git-Internals-Git-Objects)
* (Article) [Understanding git for real by exploring the .git directory](https://medium.freecodecamp.org/understanding-git-for-real-by-exploring-the-git-directory-1e079c15b807)
* (Video) [Advanced Git Tutorial](https://www.youtube.com/watch?v=0SJCYPsef54)

# Useful code snippets
**Bash find latest commits authors (branch owner) to all branches**
```bash
git for-each-ref --format='%(committerdate) %09 %(authorname) %09 %(refname)' | sort -k5n -k2M -k3n -k4n
```
**List commiters' emails which are not (grep -v) example.com**
```bash
git log --after='2018-12-01 00:00:00' | grep Author: | grep -v @example.com | sort | uniq -c | sort -n -r
```
**Compare two branches. Find all commits at Right branch which are new for Left branch. Do not include Left's commits even if they are new for Right**
```bash
git diff origin/master...origin/feature_branch > /D/diff.patch
```

**Rewrite commit messages**
- The way with intective rebase [Changing a commit message](https://help.github.com/articles/changing-a-commit-message/) see section "Amending the message of older or multiple commit messages"
- Another way with bash [Update git commit messages](https://davidwalsh.name/update-git-commit-messages)
```bash
git filter-branch --msg-filter 'echo "bug ###### - \c" && cat' master..HEAD
```
