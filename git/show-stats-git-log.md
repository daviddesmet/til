# Showing Stats in your Git Log

A simple `git log` command is going to give you a concise set of information
for each commit. Usually it is enough info. When it's not, `git log` can
provide additional information with the right flags. To include overall and
per-file stats on the number of insertions and deletions, use the `--stat`
flag.

```bash
$ git log --stat
commit 9885ff03bfd33a1e7f4290466e482e247a10427c (HEAD -> master, origin/master, origin/HEAD)
Author: David De Smet <2607383+idaviddesmet@users.noreply.github.com>
Date:   Fri Nov 16 12:02:29 2018 -0600

    Fixed link to C# category

 README.md | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)

commit b05db96d77903b62260e2bcd4fe887dc5b50b3b1
Author: David De Smet <2607383+idaviddesmet@users.noreply.github.com>
Date:   Fri Nov 16 12:00:25 2018 -0600

    Added new features from C# 8.0

 README.md                               | 20 ++++++++++++++++++--
 csharp/async-streams.md                 | 15 +++++++++++++++
 csharp/default-body-interface-member.md | 19 +++++++++++++++++++
 csharp/ranges-indices.md                | 18 ++++++++++++++++++
 csharp/recursive-patterns.md            | 15 +++++++++++++++
 csharp/switch-expressions.md            | 13 +++++++++++++
 csharp/target-typed-new-expressions.md  |  7 +++++++
 7 files changed, 105 insertions(+), 2 deletions(-)

commit 424aa62f38a04a4b23397b62ad9891beca9c9f87
Author: David De Smet <2607383+idaviddesmet@users.noreply.github.com>
Date:   Fri Oct 19 23:12:35 2018 -0500

    Update README.md

 README.md | 5 +++++
 1 file changed, 5 insertions(+)

...
```

See `man git-log` for more details.