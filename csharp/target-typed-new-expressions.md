# Target-typed new-expressions

In many cases, when we’re creating a new object, the type is already given from context. In those situations C# 8.0 will let us omit the type:

```csharp
Point[] ps = { new (1, 4), new (3,-2), new (9, 5) }; // all Points
```