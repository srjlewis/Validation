# Domain

- `Domain()`
- `Domain(bool $tldCheck)`

Validates whether the input is a valid domain name or not.

```php
v::domain()->isValid('google.com');
```

You can skip *top level domain* (TLD) checks to validate internal
domain names:

```php
v::domain(false)->isValid('dev.machine.local');
```

This is a composite validator, it validates several rules
internally:

- If input is an IP address, it fails.
- If input contains whitespace, it fails.
- If input does not contain any dots, it fails.
- If input has less than two parts, it fails.
- Input must end with a top-level-domain to pass (if not skipped).
- Each part must be alphanumeric and not start with an hyphen.
- [PunnyCode][] is accepted for [Internationalizing Domain Names in Applications][IDNA].

Messages for this validator will reflect rules above.

## Categorization

- Internet

## Changelog

Version | Description
--------|-------------
  0.6.0 | Allow to skip TLD check
  0.3.9 | Created

***
See also:

- [Ip](Ip.md)
- [Json](Json.md)
- [MacAddress](MacAddress.md)
- [PublicDomainSuffix](PublicDomainSuffix.md)
- [Tld](Tld.md)
- [Url](Url.md)

[PunnyCode]: http://en.wikipedia.org/wiki/Punycode "Wikipedia: Punnycode"
[IDNA]: http://en.wikipedia.org/wiki/Internationalized_domain_name#Internationalizing_Domain_Names_in_Applications "Wikipedia: Internationalized domain name"
