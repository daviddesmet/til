# Displaying configuration variables

Git configurationvariables can be stored at three different levels. Each level overrides values at the previous level.

1. System level (applied to every user on the system and all their repositories)

   - to view, `git config --list --system` (may need `sudo`)
   - to set, `git config --system color.ui true`
   - to edit system config file, `git config --edit --system`

2. Global level (values specific personally to you, the user)

   - to view, `git config --list --global`
   - to set, `git config --global user.name xyz`
   - to edit global config file, `git config --edit --global`
   
3. Repository level (specific to that single repository)

   - to view, `git config --list --local`
   - to set, `git config --local core.ignorecase true` (`--local` optional)
   - to edit repository config file, `git config --edit --local` (`--local` optional)

### How do I view all settings?

- Run `git config --list`, showing **system**, **global**, and (if inside a repository) **local** configs
- Run `git config --list --show-origin`, also shows the origin file of each config item

### How do I read one particular configuration?

- Run `git config user.name` to get `user.name`, for example.
- You may also specify options `--system`, `--global`, `--local` to read that value at a particular level.

[Source at Stack Overflow](https://stackoverflow.com/a/46986031)
