# Recursive patterns

C# 8.0 allows patterns to contain other patterns:

```csharp
IEnumerable<string> GetEnrollees()
{
    foreach (var p in People)
    {
        if (p is Student { Graduated: false, Name: string name }) yield return name;
    }
}
```

The pattern `Student { Graduated: false, Name: string name }` checks that the `Person` is a `Student`, then applies the constant pattern `false` to their `Graduated` property to see if they’re still enrolled, and the pattern `string name` to their `Name` property to get their name (if non-null). Thus, if `p` is a `Student`, has not graduated and has a non-null name, we `yield return` that name.