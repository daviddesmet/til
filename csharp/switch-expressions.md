# Switch expressions

Switch statements with patterns are quite powerful in C# 7.0, but can be cumbersome to write. C# 8.0 switch expressions are a “lightweight” version, where all the cases are expressions:

```csharp
var area = figure switch 
{
    Line _      => 0,
    Rectangle r => r.Width * r.Height,
    Circle c    => Math.PI * c.Radius * c.Radius,
    _           => throw new UnknownFigureException(figure)
};
```