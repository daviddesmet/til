# Ranges and indices

C# 8.0 is adding a type Index, which can be used for indexing. You can create one from an int that counts from the beginning, or with a prefix ^ operator that counts from the end:

```csharp
Index i1 = 3;  // number 3 from beginning
Index i2 = ^4; // number 4 from end
int[] a = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
Console.WriteLine($"{a[i1]}, {a[i2]}"); // "3, 6"
```

C# 8.0 is also introducing a `Range` type, which consists of two `Index`es, one for the start and one for the end, and can be written with a `x..y` _range expression_. You can then index with a `Range` in order to produce a slice:

```csharp
var slice = a[i1..i2]; // { 3, 4, 5 }
```

**NOTE:** Indexers and ranges rely on new framework types that are part of .NET Standard 2.1. This means that the types required to use these features won’t be available when you target C# 8.0 to .NET Framework 4.8.