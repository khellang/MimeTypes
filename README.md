# MimeTypes

A simple lookup from file name/extension to MIME/media type and vice versa, generated from [mime-db](https://github.com/jshttp/mime-db), which in turn is compiled from IANA, Apache and nginx's MIME types.  
This is a source-only package, containing a single class, `MimeTypes`, which will be compiled into your library/application under the root namespace.

## Installation

The easiest way to get it, is to install the source package from [NuGet.org](https://www.nuget.org/packages/MimeTypes).

Otherwise you could just pull the [source file](src/MimeTypes/MimeTypes.cs.pp) from GitHub.

## Usage

### Lookup MIME/media type for a file name/extension

Get the MIME/media type for a file name/extension by using the `MimeTypes.TryGetMimeType` or `MimeTypes.GetMimeType` methods:

```csharp
if (MimeTypes.TryGetMimeType("awesome-file.json", out var mimeType))
{
    // mimeType == "application/json"
}

MimeTypes.GetMimeType("awesome-file.json"); // "application/json"
```

When calling `GetMimeType`, if a mapping for the given file extension doesn't exist, it will fall back to `MimeTypes.FallbackMimeType`, which is set to `application/octet-stream` by default.

### Lookup file extension by MIME/media type

To get all available file extensions for a MIME/media type, you can call `MimeTypes.GetMimeTypeExtensions`. This returns back an `IEnumerable<string>` of all the available files types for the specified MIME/media type.
