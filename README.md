# MimeTypes

A simple lookup from file name/extension to MIME/media type, generated from [mime-db](https://github.com/jshttp/mime-db), which in turn is compiled from IANA, Apache and nginx's MIME types.

## Usage

Get the MIME/media type for a file name/extension by using the `MimeTypes.GetMimeType` method:

```csharp
MimeTypes.GetMimeType("awesome-file.json"); // "application/json"
```

If a mapping for the given file extension doesn't exist, it will fall back to `MimeTypes.FallbackMimeType`, which is set to `application/octet-stream` by default.

## Installation

It's just a simple, generated .cs file! To get it, either

 - Pull the checked in version from GitHub.
 - Pull the source and generate an updated version yourself. 
 - Install the [NuGet package](https://www.nuget.org/packages/MimeTypes) (contains the single source file).
