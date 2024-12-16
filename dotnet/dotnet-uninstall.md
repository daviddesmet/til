# .NET Uninstall Tool

> The .NET Uninstall tool automates removing .NET SDKs and runtimes from your system.

You can download .NET Uninstall Tool from [the tool's releases page](https://aka.ms/dotnet-core-uninstall-tool) and find the source code at the [dotnet/cli-lab](https://github.com/dotnet/cli-lab)GitHub repository.

To install it, just issue the following command:

```bash
$ sudo mkdir /usr/local/share/dotnet-tools
$ sudo tar -zxf dotnet-core-uninstall.tar.gz -C /usr/local/share/dotnet-tools/
$ dotnet tool install --global dotnet-outdated
```

Add a symbol link to the tool:

```bash
$ sudo ln -s /usr/local/share/dotnet-tools/dotnet-core-uninstall /usr/local/bin/dotnet-core-uninstall
```

Check installed .NET SDKs:

```bash
$ dotnet sdk check
```

Remove a specific SDK version:

```bash
$ sudo dotnet-core-uninstall remove 6.0.400 --sdk
```

Remove a specific runtime version:

```bash
sudo dotnet-core-uninstall remove 6.0.8 --runtime
```

