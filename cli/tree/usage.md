# `tree` is a recursive directory listing command that produces a depth-indented listing of files.

```bash
$ tree
.
├── LICENSE
├── README.md
├── cli
│   └── ack
│       ├── ignore-case.md
│       └── specific-files.md
├── csharp
│   ├── async-streams.md
│   ├── default-body-interface-member.md
│   ├── ranges-indices.md
│   ├── recursive-patterns.md
│   ├── switch-expressions.md
│   └── target-typed-new-expressions.md
├── css
│   └── dark-mode-media-query.md
├── dotnet
│   └── dotnet-outdated.md
├── git
│   ├── grab-single-file-from-stash.md
│   ├── keeping-a-fork-up-to-date.md
│   ├── push-with-noreply-address.md
│   ├── renaming-branch.md
│   ├── show-stats-git-log.md
│   ├── show-whats-in-stash.md
│   ├── stashing-untracked-files.md
│   ├── untracking-without-delete.md
│   └── viewing-file-on-another-branch.md
├── javascript
│   └── implementing-memoization.md
├── misc
│   └── wsl_open_vs_code.md
└── vue
    └── register-lifecycle-hooks-alternative.md

9 directories, 24 files
```

Specifying a maximum depth when listing:

```bash
$ tree -L 1
.
├── LICENSE
├── README.md
├── cli
├── csharp
├── css
├── dotnet
├── git
├── javascript
├── misc
└── vue

8 directories, 2 files
```
