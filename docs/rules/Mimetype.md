# Mimetype

- `Mimetype(string $mimetype)`

Validates if the input is a file and if its MIME type matches the expected one.

```php
v::mimetype('image/png')->isValid('image.png'); // true
v::mimetype('image/jpeg')->isValid('image.jpg'); // true
```

This rule is case-sensitive and requires [fileinfo](http://php.net/fileinfo) PHP extension.

## Categorization

- File system

## Changelog

Version | Description
--------|-------------
  1.0.0 | Created

***
See also:

- [Directory](Directory.md)
- [Executable](Executable.md)
- [Exists](Exists.md)
- [Extension](Extension.md)
- [File](File.md)
- [Image](Image.md)
- [Readable](Readable.md)
- [Size](Size.md)
- [SymbolicLink](SymbolicLink.md)
- [Uploaded](Uploaded.md)
- [Writable](Writable.md)
