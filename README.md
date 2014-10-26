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

### `git diff`

#### Show the files and changes that have been staged

    git diff --cached

[source](http://stackoverflow.com/questions/1587846/how-do-i-show-the-changes-which-have-been-staged)

### `git push`

#### Delete a remote branch

    git push origin --delete <branch-name>

[source](http://stackoverflow.com/a/2003515/535590)

### `git remote`

#### Change/Update the remote repository URL

    git remote set-url <remote-name> <remote-url>

    # for example, change origin url to github.com/user/repo-name
    git remote set-url origin https://github.com/user/repo-name.git

[source](http://stackoverflow.com/questions/16330404/how-to-remove-remote-origin-from-git-repo)

### `git reset`

#### Squash some commits

    # move the head back two commits as the contents of those
    # two commits gets squashed onto the index
    git reset --soft HEAD~2
    # commit the now squashed changes
    git commit

[source](http://scottchacon.com/2011/07/11/reset.html)

### `git tag`

#### Delete a remote git tag

    git tag -d v1.0.0
    git push origin :refs/tags/v1.0.0

[source](http://nathanhoad.net/how-to-delete-a-remote-git-tag)

## Links (by command)

### `git fetch`

- [What's the difference between `git pull` and `git fetch`?](http://stackoverflow.com/questions/292357/whats-the-difference-between-git-pull-and-git-fetch?rq=1)

### `git ls-files`

#### List all files staged for deletion (and then do something with them)

    # simply list the files staged for deletion
    git ls-files --deleted -z

    # perform a `git rm` on the files, putting them on the index
    git ls-files --deleted -z | xargs -0 git rm

    # perform a `git checkout --` on the files, unstaging them
    git ls-files --deleted -z | xargs -0 git checkout --

[source](http://stackoverflow.com/questions/3169787/remove-all-deleted-files-from-changed-but-not-updated-in-git)

### `git pull`

- [What's the difference between `git pull` and `git fetch`?](http://stackoverflow.com/questions/292357/whats-the-difference-between-git-pull-and-git-fetch?rq=1)
- [In what cases could `git pull` be harmful?](http://stackoverflow.com/questions/15316601/in-what-cases-could-git-pull-be-harmful)

### `git reset`

- [git reset demystified](http://scottchacon.com/2011/07/11/reset.html)
- [git reset explained](http://blog.plover.com/prog/git-reset.html)

## Workflows

- [Git-Flow](http://nvie.com/posts/a-successful-git-branching-model/)
- [GitHub-Flow](http://scottchacon.com/2011/08/31/github-flow.html)

## Resources

- [git source code on GitHub](https://github.com/git/git)
- [Pro Git book](http://git-scm.com/book)
- [git-scm reference](http://git-scm.com/docs)
- [git-scm videos](http://git-scm.com/videos)
- [Heroku Git Cheat Sheet](https://na1.salesforce.com/help/pdfs/en/salesforce_git_developer_cheatsheet.pdf)
- [Interactive Git Cheat Sheet](http://ndpsoftware.com/git-cheatsheet.html)
- [Official git Wiki](https://git.wiki.kernel.org/index.php/Main_Page)
- [Try Git interactive tutorial](http://try.github.io/)
- [Git Magic](http://www-cs-students.stanford.edu/~blynn//gitmagic/)
- [Self-hosted Git Server](https://www.petekeen.net/self-hosted-git-server)
- [Linus Torvalds on git: Google Tech Talk](https://www.youtube.com/watch?v=4XpnKHJAok8)
- [r/git](http://www.reddit.com/r/git/)
- [git ready](http://gitready.com/)
- [git for computer scientists](http://eagain.net/articles/git-for-computer-scientists/)
- [a git tutorial and primer](http://www.danielmiessler.com/study/git/)
- [Ry's Git Tutorial](http://rypress.com/tutorials/git/index.html)
- [git immersion](http://gitimmersion.com/)
- [think like a git](http://think-like-a-git.net/)
- [Visualizing Git Concepts with D3](http://www.wei-wang.com/ExplainGitWithD3) ([GitHub repo](https://github.com/onlywei/explain-git-with-d3))
- [git - the simple guide](http://rogerdudler.github.io/git-guide/)
- [Changing history, or How to git pretty](http://justinhileman.info/article/changing-history/)
- [git cheat sheet](http://cheat.errtheblog.com/s/git)
- [How to handle big repositories with git](http://blogs.atlassian.com/2014/05/handle-big-repositories-git/)
- [Ry's Git Tips and Tricks](http://rypress.com/tutorials/git/tips-and-tricks.html)
- [25 Tips for Intermediate Git Users](http://www.andyjeffries.co.uk/25-tips-for-intermediate-git-users/)
- [A few git tips you didn't know about](http://mislav.uniqpath.com/2010/07/git-tips/)
- [Things you didn't know about Git](http://www.matheuslima.com/things-you-didnt-know-about-git/)
- [A Hacker's Guide to Git](http://wildlyinaccurate.com/a-hackers-guide-to-git)
- [Git merge vs. rebase](http://mislav.uniqpath.com/2013/02/merge-vs-rebase/)
- [Git Fetch and Merge](http://longair.net/blog/2009/04/16/git-fetch-and-merge/)
- [Using topic branches and interactive rebasing effectively](https://blog.mozilla.org/webdev/2011/11/21/git-using-topic-branches-and-interactive-rebasing-effectively/)
- [Move a subdirectory from one git repository to a subdirectory of another,
  without losing commit
  history](https://gist.github.com/smashwilson/015e6a3abfbf7af73d31)

### Commit Messages

- [A Note About Git Commit Messages](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
- [5 Useful Tips For A Better Commit Message](http://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message)
