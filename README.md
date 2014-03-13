# man-git

a collection of git tips and tricks

## Tips and Tricks (by command)

### `git branch`

#### Delete a local branch

    git branch -d <branch-name>

[source](http://stackoverflow.com/a/10999165/535590)

#### Delete an unmerged local branch

    git branch -D <branch-name>

source: git man pages

### `git checkout`

#### Checkout specific file from another branch

    git checkout <branch_name> -- <paths>

[source](http://nicolasgallagher.com/git-checkout-specific-files-from-another-branch/)

### `git push`

#### Delete a remote branch

    git push origin --delete <branch-name>

[source](http://stackoverflow.com/a/2003515/535590)

### `git tag`

#### Delete a remote git tag

    git tag -d v1.0.0
    git push origin :refs/tags/v1.0.0

[source](http://nathanhoad.net/how-to-delete-a-remote-git-tag)

## Links (by command)

### `git reset`

- [git reset explained](http://blog.plover.com/prog/git-reset.html)

## Resources

- [git source code on GitHub](https://github.com/git/git)
- [Pro Git book](http://git-scm.com/book)
- [git-scm reference](http://git-scm.com/docs)
- [git-scm videos](http://git-scm.com/videos)
- [Heroku Git Cheat Sheet](https://na1.salesforce.com/help/pdfs/en/salesforce_git_developer_cheatsheet.pdf)
- [Interactive Git Cheat Sheet](http://ndpsoftware.com/git-cheatsheet.html)
- [Official git Wiki](https://git.wiki.kernel.org/index.php/Main_Page)
- [Try Git interactive tutorial](http://try.github.io/)
