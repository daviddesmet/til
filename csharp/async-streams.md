# Async streams

C# 8.0 introduce `IAsyncEnumerable<T>`, which is exactly what we’d expect; an asynchronous version of `IEnumerable<T>`. The language lets you `await foreach` over these to consume their elements, and `yield return` to them to produce elements.

```csharp
async IAsyncEnumerable<int> GetBigResultsAsync()
{
    await foreach (var result in GetResultsAsync())
    {
        if (result > 20) yield return result; 
    }
}
```

**NOTE:** Async streams rely on new framework types that are part of .NET Standard 2.1. This means that the types required to use these features won’t be available when you target C# 8.0 to .NET Framework 4.8.