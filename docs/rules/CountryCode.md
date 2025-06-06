# CountryCode

- `CountryCode()`
- `CountryCode(string $set)`

Validates whether the input is a country code in [ISO 3166-1][] standard.

```php
v::countryCode()->isValid('BR'); // true

v::countryCode('alpha-2')->isValid('NL'); // true
v::countryCode('alpha-3')->isValid('USA'); // true
v::countryCode('numeric')->isValid('504'); // true
```

This rule supports the three sets of country codes:

- ISO 3166-1 alpha-2 (`'alpha-2'` or `CountryCode::ALPHA2`)
- ISO 3166-1 alpha-3 (`'alpha-3'` or `CountryCode::ALPHA3`)
- ISO 3166-1 numeric (`'numeric'` or `CountryCode::NUMERIC`).

When no set is defined the rule uses `'alpha-2'` (`CountryCode::ALPHA2`).

This rules uses data from [iso-codes][].

## Categorization

- ISO codes
- Localization

## Changelog

Version | Description
--------|-------------
  2.0.0 | Became case-sensitive
  0.5.0 | Created

***
See also:

- [CurrencyCode](CurrencyCode.md)
- [LanguageCode](LanguageCode.md)
- [PostalCode](PostalCode.md)
- [PublicDomainSuffix](PublicDomainSuffix.md)
- [SubdivisionCode](SubdivisionCode.md)
- [Tld](Tld.md)

[ISO 3166-1]: https://wikipedia.org/wiki/ISO_3166-1
[iso-codes]: https://salsa.debian.org/iso-codes-team/iso-codes
