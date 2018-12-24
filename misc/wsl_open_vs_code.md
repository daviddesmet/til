# Open Visual Studio Code from WSL

With [interoperability](https://msdn.microsoft.com/en-us/commandline/wsl/interop), 
you can open Windows programs from WSL. This delivers a seamless experience between Windows and WSL.

Let's begin by creating a symlink to VS Code's Windows binary:

```bash
sudo ln -s /c/Users/[USERNAME]/AppData/Local/Programs/Microsoft\ VS\ Code/Code.exe code
```

Now you will be able to issue `code .` in any directory within the wsl console.
