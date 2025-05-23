# Max

- `Max(mixed $compareTo)`

Validates whether the input is less than or equal to a value.

```php
v::max(10)->isValid(9); // true
v::max(10)->isValid(10); // true
v::max(10)->isValid(11); // false
```

Validation makes comparison easier, check out our supported
[comparable values](../07-comparable-values.md).

Message template for this validator includes `{{compareTo}}`.

## Categorization

- Comparisons

## Changelog

Version | Description
--------|-------------
  2.0.0 | Became always inclusive
  1.0.0 | Became inclusive by default
  0.3.9 | Created

***
See also:

- [Between](Between.md)
- [GreaterThan](GreaterThan.md)
- [LessThan](LessThan.md)
- [MaxAge](MaxAge.md)
- [Min](Min.md)
- [MinAge](MinAge.md)
