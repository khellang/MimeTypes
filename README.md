# MimeTypes

A simple lookup from file extension to MIME type, generated from the Apache registry

## Usage

Get the MIME type for a file by using the `MimeTypes.GetMimeType` method:

```csharp
MimeTypes.GetMimeType("awesome-file.json"); // "application/json"
```

## Installation

It's just a simple, generated .cs file! To get it, either

 - Pull the checked in version from GitHub.
 - Pull the source and generate an updated version yourself. 
 - Install the [NuGet package]() (contains the single source file).