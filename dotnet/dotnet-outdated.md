# Keeping dependencies up to date with dotnet-outdated

Similarly as [yarn outdated](https://yarnpkg.com/lang/en/docs/cli/outdated/), [npm outdated](https://docs.npmjs.com/cli/outdated) and [paket outdated](https://fsprojects.github.io/Paket/paket-outdated.html), there's [dotnet outdated](https://github.com/jerriep/dotnet-outdated) created by [Jerrie Pelser](https://github.com/jerriep).

To install it, just issue the following command:

```bash
$ dotnet tool install --global dotnet-outdated
```

Or update it with:

```bash
$ dotnet tool update --global dotnet-outdated
```

**_dotnet-outdated_** can automatically attempt to upgrade any outdated packages to the latest version by passing the `-u|--upgrade` option. You can let **_dotnet-outdated_** prompt you for each outdated package by using the `-u:prompt` option.

**NOTE:** [.NET Core 2.1 SDK](https://www.microsoft.com/net/download) or newer is required.