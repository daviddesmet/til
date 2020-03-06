# Push a commit with a GitHub noreply address

1. Change the global user e-mail address setting to be your GitHub noreply address:

```bash
$ git config --global user.email {ID}+{username}@users.noreply.github.com
```

2. Reset the author information on your last commit:

```bash
$ git commit --amend --reset-author
```

3. Now you can push the commit with the noreply e-mail address, and future commits will have the noreply e-mail address as well. Use the `push --force` command to force push over the old commit

```bash
$ git push
```

[Source at Stack Overflow](https://stackoverflow.com/questions/43378060/meaning-of-the-github-message-push-declined-due-to-email-privacy-restrictions)
