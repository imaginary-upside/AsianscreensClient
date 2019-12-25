# Asianscreens Client
An asianscreens.com scraper library implemented in C#.

# Usage
```csharp
var client = new Asianscreens.Client();

var actress1 = await client.SearchFirst("Ai Uehara");

var actresses = await client.Search("Ai Uehara");
var actress2 = await client.LoadVideo(actresses.First().id);

// actress1 == actress2

foreach (var actress in await client.Search("Ai"))
    System.Console.WriteLine(actress.Name);
```

# License
Licensed under AGPL-3.0-only
