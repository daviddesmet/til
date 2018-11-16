# Viewing a file on another Branch

Sometimes you want to view a file on another branch (without switching
branches). That is, you want to view the version of that file as it exists
on that branch. `git show` can help. If your branch is named `xfeature` and
the file you want to see is `app/models/users.js`, then your command should
look like this:

```
$ git show xfeature:app/models/users.js
```

You can even tab-complete the filename as you type it out.

See `man git-show` for more details.

[Source at Stack Overflow](http://stackoverflow.com/questions/7856416/view-a-file-in-a-different-git-branch-without-changing-branches)