# Repository Setup

## Versioning an existing project with a new repository

Navigate to the root folder and execute:

```bash
$ git init
```

## Cloning an existing repository

```bash
$ git clone <remote url>
```

## Configure the upstream (remote) branch:

```bash
$ git remote add upstream <remote url>
```

Where `upstream` is the remote name.

## Push local changes to upstream:

```bash
$ git push
```

or 

```bash
$ git push -u <remote_name> <local_branch_name>
```

## Setting the author details

The author details can be set globally (system-wide) or locally (per repository).

```bash
$ git config --global user.name <name>
$ git config --local user.email <email>
```
