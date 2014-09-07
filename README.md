# MimeTypes

A simple lookup from file name/extension to MIME/media type, generated from Apache's [mime.types](https://svn.apache.org/repos/asf/httpd/httpd/trunk/docs/conf/mime.types)

## Usage

Get the MIME/media type for a file name/extension by using the `MimeTypes.GetMimeType` method:

```csharp
MimeTypes.GetMimeType("awesome-file.json"); // "application/json"
```

## Installation

It's just a simple, generated .cs file! To get it, either

 - Pull the checked in version from GitHub.
 - Pull the source and generate an updated version yourself. 
 - Install the [NuGet package](https://www.nuget.org/packages/MimeTypes) (contains the single source file).
