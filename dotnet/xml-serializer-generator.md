# Using Microsoft XML Serializer Generator

Like the [Xml Serializer Generator (sgen.exe)](https://docs.microsoft.com/en-us/dotnet/standard/serialization/xml-serializer-generator-tool-sgen-exe) for the .NET Framework, the [Microsoft.XmlSerializer.Generator NuGet package](https://www.nuget.org/packages/Microsoft.XmlSerializer.Generator) is the equivalent for .NET Core and .NET Standard projects.

Add the following reference to the project:

```bash
$ dotnet add package Microsoft.XmlSerializer.Generator -v 1.0.0
```

The above command will create the entry in the csproj file:

```xml
<ItemGroup>
   <PackageReference Include="Microsoft.XmlSerializer.Generator" Version="1.0.0" />
</ItemGroup>
```

Finally, add the following section after the previous entry for the CLI Tool support:

```xml
<ItemGroup>
   <DotNetCliToolReference Include="Microsoft.XmlSerializer.Generator" Version="1.0.0" />
</ItemGroup>
```

**NOTE:** [.NET Core 2.1 SDK](https://www.microsoft.com/net/download) or newer is required.
