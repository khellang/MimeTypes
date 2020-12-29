# MimeTypes

A simple lookup from file name/extension to MIME/media type, generated from [mime-db](https://github.com/jshttp/mime-db), which in turn is compiled from IANA, Apache and nginx's MIME types.

## Installation

The easiest way to get it, is to install the source package from [NuGet.org](https://www.nuget.org/packages/MimeTypes).

Otherwise you could just pull the [source file](src/MimeTypes/MimeTypes.cs.pp) from GitHub.

## Usage

Get the MIME/media type for a file name/extension by using the `MimeTypes.GetMimeType` method:

```csharp
MimeTypes.GetMimeType("awesome-file.json"); // "application/json"
```

If a mapping for the given file extension doesn't exist, it will fall back to `MimeTypes.FallbackMimeType`, which is set to `application/octet-stream` by default.
