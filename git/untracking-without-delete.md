# Untracking a file or directory without deleting it

Generally when I invoke `git rm <filename>`, I do so with the intention of
removing a file from the project entirely. `git-rm` does exactly that,
removing the file both from the index and from the working tree.

If you want to untrack a file (remove it from the index), but still have it
available locally (in the working tree), then you are going to want to use
the `--cached` flag.

```bash
$ git rm --cached <filename>
```

If you do this, you may also consider adding that file to the `.gitignore`
file.

The same can be done for a directory of files that you don't want tracked. Just use the -r flag:

```bash
$ git rm --cached -r <directory>
```

[Source at Stack Overflow](http://stackoverflow.com/questions/15027873/untrack-and-stop-tracking-files-in-git)
[Source at Stack Overflow](http://stackoverflow.com/questions/1143796/remove-a-file-from-a-git-repository-without-deleting-it-from-the-local-filesyste)