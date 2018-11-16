# Default implementations of interface members

In C# 8.0 we can provide a body for an interface member:

```csharp
interface ILogger
{
    void Log(LogLevel level, string message);
    void Log(Exception ex) => Log(LogLevel.Error, ex.ToString()); // New overload
}

class ConsoleLogger : ILogger
{
    public void Log(LogLevel level, string message) { ... }
    // Log(Exception) gets default implementation
}
```

The ConsoleLogger class doesn’t have to implement the `Log(Exception)` overload of `ILogger`, because it is declared with a default implementation.